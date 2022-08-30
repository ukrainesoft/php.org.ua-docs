Задає ім'я модулю

-   [« ocisetedition](function.oci-set-edition.html)
    
-   [ocisetprefetchlob »](function.oci-set-prefetch-lob.html)
    
-   [PHP Manual](index.md)
    
-   [OCI8 Функции](ref.oci8.md)
    
-   Задає ім'я модулю
    

# ocisetmodulename

(PHP 5> = 5.3.2, PHP 7, PHP 8, PECL OCI8> = 1.4.0)

ocisetmodulename — Вказує ім'я модуля

### Опис

```methodsynopsis
oci_set_module_name(resource $connection, string $name): bool
```

Вказує ім'я модуля для трасування Oracle.

Ім'я модуля реєструється в базі даних під час чергового запиту PHP, наприклад, коли запускається SQL вираз.

Ім'я може бути витягнуте з адміністративних уявлень бази даних, таких як `V$SESSION`. Воно може використовуватися для трасування та моніторингу також, як `V$SQLAREA` and `DBMS_MONITOR.SERV_MOD_ACT_STAT_ENABLE`

Значення можна встановлювати через постійні з'єднання.

### Список параметрів

`connection`

Ідентифікатор з'єднання Oracle, що повертається [ociconnect()](function.oci-connect.html) [ocipconnect()](function.oci-pconnect.html), або [ocinewconnect()](function.oci-new-connect.html)

`name`

Заданий користувачем рядок string довжиною до 48 байт.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Встановлення імені модуля**

```php
<?php

$c = oci_connect('hr', 'welcome', 'localhost/XE');

// Запись модуля
oci_set_module_name($c, 'Home Page');

// Код, осуществляющий запрос к БД, например выборка:
$s = oci_parse($c, 'select * from dual');
oci_execute($s);
oci_fetch_all($s, $res);

sleep(30);
?>
```

```
// Пока скрипт выполняется, администратор может увидеть, какие модули
// используются:

sqlplus system/welcome
SQL> select module from v$session;
```

### Примітки

> **Зауваження** **Вимога до версії Oracle**
> 
> Ця функція доступна, якщо PHP злінковано з бібліотеками Oracle Database починаючи з версії 10*г* і вище.

**Підказка**

# Продуктивність

У старих версіях OCI8 або бази даних Oracle можна було встановити інформацію про клієнта за допомогою пакета `DBMS_APPLICATION_INFO`. Для цієї мети ефективніше використання функції [ocisetclientinfo()](function.oci-set-client-info.html)

**Застереження**

# Порада щодо повного сканування таблиці (roundtrip)

Деякі, але не всі функції OCI8 викликають повне сканування таблиці (roundtrip). Повне сканування таблиць немає для тих запитів, у яких включено кешування результатів у базі даних.

### Дивіться також

-   [ocisetaction()](function.oci-set-action.html) - Вказує ім'я для дії
-   [ocisetclientinfo()](function.oci-set-client-info.html) - Задає інформацію про клієнта
-   [ocisetclientidentifier()](function.oci-set-client-identifier.html) - задає ідентифікатор клієнта
-   [ocisetдбoperation()](function.oci-set-db-operation.html) - Задає операцію бази даних