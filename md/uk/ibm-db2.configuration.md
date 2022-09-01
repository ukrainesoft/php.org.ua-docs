---
navigation:
  - ibm-db2.installation.html: « Установка
  - ibm-db2.resources.html: Типи ресурсів »
  - index.md: PHP Manual
  - ibm-db2.setup.html: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**ibmdb2 Опції налаштування**

| Имя | По умолчанию | Место изменения | Лог изменений |
| --- | --- | --- | --- |
| [ibmdb2.binmode](ibm-db2.configuration.html#ini.ibm-db2.binmode) | "1" | PHPINIALL |  |
| [ibmdb2.i5allpconnect](ibm-db2.configuration.html#ini.ibm-db2.i5-all-pconnect) | "0" | PHPINISYSTEM | Доступно з ibmdb2 1.6.5. |
| [ibmdb2.i5allowcommit](ibm-db2.configuration.html#ini.ibm-db2.i5-allow-commit) | "0" | PHPINISYSTEM | Доступно з ibmdb2 1.4.9. |
| [ibmdb2.i5dbcsalloc](ibm-db2.configuration.html#ini.ibm-db2.i5-dbcs-alloc) | "0" | PHPINISYSTEM | Доступно з ibmdb2 1.5.0. |
| [ibmdb2.instancename](ibm-db2.configuration.html#ini.ibm-db2.instance-name) | NULL | PHPINISYSTEM | Доступно з ibmdb2 1.0.2. |
| [ibmdb2.i5ignoreuserid](ibm-db2.configuration.html#ini.ibm-db2.i5-ignore-userid) | "0" | PHPINISYSTEM | Доступно з ibmdb2 1.8.0. |

Коротке пояснення конфігураційних директив.

`ibm_db2.binmode` int

Ця опція контролює режим конвертації з/в бінарні дані у програмі PHP.

-   1 (DB2BINARY)
    
-   2 (DB2CONVERT)
    
-   3 (DB2PASSTHRU)
    

`ibm_db2.i5_all_pconnect` int

Ця опція повністю перевизначає поведінку i5 [db2connect()](function.db2-connect.html). Якщо `ibm_db2.i5_all_pconnect` = 1, всі з'єднання з DB2 будуть постійними ([db2pconnect()](function.db2-pconnect.html)). На i5/OS використовувати [db2pconnect()](function.db2-pconnect.html) набагато, категорично, краще ніж [db2connect()](function.db2-connect.html). Ця установка перевизначає [db2connect()](function.db2-connect.html) таким чином, що завжди викликається [db2pconnect()](function.db2-pconnect.md)що дозволяє не переписувати код програми.

-   [db2connect()](function.db2-connect.md) працює штатно
    
-   [db2connect()](function.db2-connect.html) працює як [db2pconnect()](function.db2-pconnect.md)
    

`ibm_db2.i5_allow_commit` int

Ця опція контролює рівень ізоляції, що використовується для i5 схеми колекцій у додатку PHP (див. `i5_commit` для перевизначення).

-   0 – контроль зобов'язань не використовується.
    
-   1 - read uncommitted, можливо брудне читання.
    
-   2 - read committed, брудне читання неможливо.
    
-   3 - repeatable read, брудне і неповторне читання не можливі.
    
-   4 - serializeable, брудне читання, неповторне читання і фантоми не можливі.
    

`ibm_db2.i5_dbcs_alloc` int

Ця опція контролює внутрішню схему розташування великих буферів колонок DBCS.

-   0 - немає розширеного розміщення (дивися `i5_dbcs_alloc` для перевизначення)
    
-   1 - використовувати розширене розміщення (дивися `i5_dbcs_alloc` для перевизначення)
    

`ibm_db2.instance_name` string

В операційних системах Linux і UNIX ця опція задає ім'я екземпляра для використання каталогізованих з'єднань з базою даних. Якщо ця опція визначена, її значення використовується замість змінної оточення DB2INSTANCE.

Ця опція ігнорується у Windows.

`ibm_db2.i5_ignore_userid` int

Ця опція перевизначає userid та password для i5 db2(p)connect в програмі PHP. Якщо `ibm_db2.i5_ignore_userid` = 1, всі з'єднання будуть відбуватися з userid=**`null`** та password=**`null`**. Отже завдання Apache з'єднуватимуться з поточним профайлом (NOBODY). Використовуйте це перевизначення тільки для простих сайтів, які не потребують перемикання профайлів і, отже, зможете уникнути всіх витрат накладних пов'язаних з додатковими завданнями QSQSRVR. Це просте рішення для обнулення userid та password без внесення змін до коду PHP. Це перевизначення можна використовувати разом з `ibm_db2.i5_all_pconnect`

-   0 - db2(p)connect використовує передані userid та password
    
-   1 - db2(p)connect вважає userid та password за **`null`**
