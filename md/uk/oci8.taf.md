- [« Підтримка OCI8 Fast Application Notification
(FAN)](oci8.fan.md)
- [OCI8 та динамічне трасування DTrace »](oci8.dtrace.md)

- [PHP Manual](index.md)
- [OCI8](book.oci8.md)
- Підтримка прозорого для програм відновлення після відмови
(Transparent Application Failover або TAF) для OCI8

# Підтримка прозорого для програм відновлення після відмови (Transparent Application Failover або TAF) для OCI8

TAF - це механізм бази даних Oracle, що забезпечує високу
доступність. Він дозволяє програмам PHP використовуючим OCI8
автоматично перепідключатися до резервної бази даних у разі збою на
основний або при мережевих проблемах.

У конфігурованій системі бази даних Oracle, TAF відбувається коли
програма PHP визначає, що екземпляр бази даних недоступний. В цьому
У випадку відбувається з'єднання з іншим вузлом в Oracle
[» RAC](https://www.oracle.com/pls/topic/lookup?ctx=dblatest&id=GUID-DEF850F6-27E9-428E-B8FC-530230D78AD2).
Це може бути гарячий резерв або той самий екземпляр бази даних.
Докладніше про OCI TAF читайте в Oracle Oracle Interface Programmer's
Guide](https://www.oracle.com/pls/topic/lookup?ctx=dblatest&id=GUID-F7817CD2-4A2C-4D37-BD36-56DBABD4725F).

Ви можете зареєструвати функцію зворотного дзвінка для програми.
[oci_register_taf_callback()](function.oci-register-taf-callback.md).
У процесі відновлення після відмови виконання програми буде
призупинено та буде викликано зареєстровану функцію зворотного
виклику. Ця функція сповіщатиме додаток про події процесу
відновлення. Якщо відновлення завершилося успішно, керування
буде повернено додатком. Якщо відновлення завершилося невдало,
всі наступні звернення до бази даних будуть завершуватися з помилкою,
оскільки відсутнє підключення.

Коли з'єднання переходить до іншої бази даних, зворотний дзвінок може
скинути будь-який необхідний стан з'єднання, наприклад, перевиконати
будь-яку необхідну команду ALTER SESSION якщо для сервісу бази даних не
увімкнено -failover_restore.

Реєстрацію зворотного дзвінка можна видалити за допомогою
[oci_unregister_taf_callback()](function.oci-unregister-taf-callback.md).

## налаштування TAF

TAF можна настроїти на стороні PHP OCI8 або конфігурації бази даних.
Якщо налаштовано і там, і там, то перевага віддається настройкам на
стороні бази даних.

Налаштувати TAF у PHP OCI8 (на стороні клієнта) можна додавши параметр
FAILOVER_MODE є частиною CONNECT_DATA дескриптора з'єднання. Більше
детально про налаштування TAF на стороні клієнта читайте в [» Oracle
Database Net Services Administrator's Guide](https://www.oracle.com/pls/topic/lookup?ctx=dblatest&id=GUID-8F532535-C401-4B51-BE0B-04FD74BB0621).

Приклад налаштування TAF в tnsnames.ora для перепідключення до тієї ж самої
БД:

ORCL =
(DESCRIPTION =
(ADDRESS = (PROTOCOL = TCP) (HOST = 127.0.0.1) (PORT = 1521))
(CONNECT_DATA =
(SERVICE_NAME = orclpdb1)
(FAILOVER_MODE =
(TYPE = SELECT)
(METHOD = BASIC)
(RETRIES = 20)
(DELAY = 15))))

Також можна настроїти TAF на стороні бази даних шляхом модифікації
сервісу за допомогою
[»srvctl](https://www.oracle.com/pls/topic/lookup?ctx=dblatest&id=GUID-8DC4D5E0-CA9D-47BC-BAD0-8769405AFEC5)
(для RAC) або за допомогою пакетної процедури [» DBMS_SERVICE.MODIFY_SERVICE](https://www.oracle.com/pls/topic/lookup?ctx=dblatest&id=GUID-C11449DC-EEDE-4BB8-9D2C-0A45198C1928)
(Для одиночних екземплярів баз даних).

## Використання функцій зворотного виклику TAF у OCI8

Функція зворотного виклику TAF є функцією, зареєстрованою з
програми для запуску у процесі відновлення після збою. При
відновлення з'єднання вона викликається кілька разів.

Перший раз вона запускається у момент виявлення проблем зі з'єднанням.
Це дозволяє програмі коректно підготуватися до затримки виконання
на час відновлення після збою. Якщо відновлення завершилося
Успішно, функція буде викликана відразу після відновлення підключення.
Цей запуск програма може використовуватись для пересинхронізації налаштувань
сесії та оповіщення користувача про те, що відбулося відновлення
після збою. Якщо відновлення завершилося невдало, функція
запускається ще раз для оповіщення програми про те, що відновлення
завершилося з помилкою та з'єднання з БД недоступне.

Інтерфейс функції зворотного виклику TAF:

**userCallbackFn**(resource `$connection`, int `$event`, int `$type`):
int

`connection`
Ідентифікатор з'єднання Oracle для якого ця функція була
зареєстрована за допомогою
[oci_register_taf_callback()](function.oci-register-taf-callback.md).
З'єднання недоступне під час аварійного відновлення.

`event`
Подія відновлення означає поточний статус відновлення.

- **`OCI_FO_BEGIN`** означає, що сталася втрата з'єднання та
процес відновлення розпочато.

- **`OCI_FO_END`** означає вдале відновлення з'єднання.

- **`OCI_FO_ABORT`** означає, що відновлення завершилося невдало
та спроб відновлення більше не буде.

- **`OCI_FO_ERROR`** також означає, що відновлення завершилося з
помилкою, але додатку дається можливість обробити помилку та
повернути OCI_FO_RETRY ще для однієї спроби відновлення.

- **`OCI_FO_REAUTH`** означає, що користувач Oracle був повторно
автентифікований.

`type`
Тип відновлення після відмови. Це дозволяє функції зрозуміти, який тип
відновлення запитаний додатком. Допустимі такі значення:

- **`OCI_FO_SESSION`** означає, що користувач запросив тільки
відновлення сесії. Наприклад, якщо з'єднання зникло, то буде
створено нову сесію на резервному сервері. Цей тип відновлення
не намагатиметься відновити запити типу SELECT.

- **`OCI_FO_SELECT`** означає, що запрошено відновлення запитів
SELECT. Це дозволить використовувати відкритий курсор для отримання
значень після відновлення.

`return value`
- **`0`** означає, що кроки відновлення після відмови мають
продовжуватись нормально.

- **`OCI_FO_RETRY`** означає, що необхідно спробувати
відновити ще раз. У разі виникнення помилки під час переходу
нове з'єднання TAF може повторити перехід на інший ресурс.
Зазвичай, перед поверненням коду OCI_FO_RETRY рекомендується деяке
час зачекати.

Приклад реєстрації функції зворотного дзвінка TAF



## Також дивіться

- [oci_register_taf_callback()](function.oci-register-taf-callback.md)
- [oci_unregister_taf_callback()](function.oci-unregister-taf-callback.md)
