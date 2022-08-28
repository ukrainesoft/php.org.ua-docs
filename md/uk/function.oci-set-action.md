Вказує ім'я для дії

-   [« oci\_server\_version](function.oci-server-version.html)
    
-   [oci\_set\_call\_timeout »](function.oci-set-call-timout.html)
    
-   [PHP Manual](index.html)
    
-   [OCI8 Функции](ref.oci8.html)
    
-   Вказує ім'я для дії
    

# ocisetaction

(PHP 5> = 5.3.2, PHP 7, PHP 8, PECL OCI8> = 1.4.0)

ocisetaction — Вказує ім'я для дії

### Опис

```methodsynopsis
oci_set_action(resource $connection, string $action): bool
```

Надає ім'я дії для трасування Oracle.

Надане ім'я реєструється в базі даних під час чергового запиту від PHP, наприклад, коли запускається SQL вираз.

Ім'я дії може бути витягнуте з адміністративних уявлень бази даних, таких як `V$SESSION`. Його можна використовувати для трасування та моніторингу, наприклад, за допомогою `V$SQLAREA` і `DBMS_MONITOR.SERV_MOD_ACT_STAT_ENABLE`

Значення можна встановлювати через постійні з'єднання.

### Список параметрів

`connection`

Ідентифікатор з'єднання Oracle, що повертається [oci\_connect()](function.oci-connect.html) [oci\_pconnect()](function.oci-pconnect.html), або [oci\_new\_connect()](function.oci-new-connect.html)

`action`

Заданий користувачем рядок до 32 байт.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Встановлення дії**

```php
<?php

$c = oci_connect('hr', 'welcome', 'localhost/XE');

// Запись действия
oci_set_action($c, 'Friend Lookup');

// Код, осуществляющий запрос к БД, например выборка:
$s = oci_parse($c, 'select * from dual');
oci_execute($s);
oci_fetch_all($s, $res);

sleep(30);

?>
```

```
// Пока скрипт выполняется, администратор может наблюдать выполнение действий:

sqlplus system/welcome
SQL> select action from v$session;
```

### Примітки

> **Зауваження** **Вимога до версії Oracle**
> 
> Ця функція доступна, якщо PHP злінковано з бібліотеками Oracle Database починаючи з версії 10*г* і вище.

**Підказка**

# Продуктивність

У старих версіях OCI8 або бази даних Oracle можна було встановити інформацію про клієнта за допомогою пакета `DBMS_APPLICATION_INFO`. Для цієї мети ефективніше використання функції [oci\_set\_client\_info()](function.oci-set-client-info.html)

**Застереження**

# Порада щодо повного сканування таблиці (roundtrip)

Деякі, але не всі функції OCI8 викликають повне сканування таблиці (roundtrip). Повне сканування таблиць немає для тих запитів, у яких включено кешування результатів у базі даних.

### Дивіться також

-   [oci\_set\_module\_name()](function.oci-set-module-name.html) - Задає ім'я модулю
-   [oci\_set\_client\_info()](function.oci-set-client-info.html) - Задає інформацію про клієнта
-   [oci\_set\_client\_identifier()](function.oci-set-client-identifier.html) - задає ідентифікатор клієнта
-   [oci\_set\_db\_operation()](function.oci-set-db-operation.html) - Задає операцію бази даних