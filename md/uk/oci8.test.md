- [« Установка](oci8.installation.md)
- [Налаштування під час виконання »](oci8.configuration.md)

- [PHP Manual](index.md)
- [Встановлення та налаштування](oci8.setup.md)
- Тестування

## Тестування

Набір тестів для OCI8 знаходиться у директорії `ext/oci8/tests`. Після
прогону цих тестів, у цій директорії також опиняться файли журналів
подій, що відбулися, і помилок.

Перед запуском тестів необхідно відредагувати файл `details.inc` та
встановити значення змінним $user, $password і рядку з'єднання $dbase.
Набір тестів OCI8 розроблявся з використанням облікового запису
`SYSTEM`. Деякі тести не виконуватимуться, якщо у тестуючого
користувача немає аналогічних прав доступу.

Для тестування функції Oracle створення пулів з'єднань (Database
Resident Connection Pooling) необхідно встановити змінну $test_drcp
в **`true`**, а також переконайтеся, що у рядку з'єднання заданий
відповідна адреса DRCP сервера.

Як альтернативу редагування файлу `details.inc` можна задати
значення змінним оточення, наприклад:

$ export PHP_OCI8_TEST_USER=system
$ export PHP_OCI8_TEST_PASS=oracle
$ export PHP_OCI8_TEST_DB=localhost/XE
$ export PHP_OCI8_TEST_DRCP=FALSE

Зверніть увагу, що у деяких оболонках ці змінні можуть
неправильно транслюватися в PHP процес, і у тестах виникатимуть
помилки підключення до бази даних. Будьте обережні при використанні
цього методу налаштування модуля.

Далі необхідно встановити оточення бази даних Oracle. Якщо ви
використовуєте PHP на тих же машинах, що і Oracle Database, ви можете
запустити:

$. /usr/local/bin/oraenv

Для Oracle 11*g*R2 XE:

$. /u01/app/oracle/product/11.2.0/xe/bin/oracle_env.sh

Деякі оболонки вимагають, щоб у `php.ini` параметр variables_order
містив літеру `E`, наприклад:

variables_order = "EGPCS"

Запуск всіх тестів PHP можна здійснити командою:

$ cd your_php_src_directory
$ make test

або можна запустити тільки OCI8 тести:

$ cd your_php_src_directory
$ make test TESTS=ext/oci8

Після завершення тестування перегляньте журнали на наявність помилок. На
слабких машинах час виконання деяких тестів може перевищити
значення налаштування часу очікування у файлі `run-tests.php`. Щоб це
виправити, задайте змінній оточення `TEST_TIMEOUT` значення більше
(Значення в секундах).

На швидких обчислювальних системах з локальною базою даних
розрахованих на невеликі навантаження (наприклад, Oracle 11*g*R2 XE),
деякі тести можуть викликати помилки ORA-12516 або ORA-12520. Для їх
запобігання необхідно збільшити значення параметра бази даних
`PROCESSES` за інструкцією нижче:

Підключитися до бази даних у ролі суперкористувача:

$ su - oracle

Задати необхідне оточення за допомогою сценаріїв `oracle_env.sh` або
`oraenv`, як описано вище.

Запустити утиліту командного рядка SQL\Plus та збільшити значення
`PROCESSES`

$sqlplus/as sysdba
SQL> alter system set processes=100 scope=spfile

Перезапустити базу даних:

SQL> startup force
