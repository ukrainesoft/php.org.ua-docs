Задає інформацію про клієнта

-   [« oci\_set\_client\_identifier](function.oci-set-client-identifier.html)
    
-   [oci\_set\_db\_operation »](function.oci-set-db-operation.html)
    
-   [PHP Manual](index.html)
    
-   [OCI8 Функции](ref.oci8.html)
    
-   Задає інформацію про клієнта
    

# ocisetclientinfo

(PHP 5> = 5.3.2, PHP 7, PHP 8, PECL OCI8> = 1.4.0)

ocisetclientinfo — Задає інформацію про клієнта

### Опис

```methodsynopsis
oci_set_client_info(resource $connection, string $client_info): bool
```

Зачепить інформацію про клієнта для трасування Oracle.

Інформація про клієнта реєструється в базі даних під час чергового запиту PHP, наприклад, коли запускається SQL вираз.

Клієнтська інформація може бути вилучена з адміністративних уявлень бази даних, таких як `V$SESSION`

Значення можна встановлювати через постійні з'єднання.

### Список параметрів

`connection`

Ідентифікатор з'єднання Oracle, що повертається [oci\_connect()](function.oci-connect.html) [oci\_pconnect()](function.oci-pconnect.html), або [oci\_new\_connect()](function.oci-new-connect.html)

`client_info`

Заданий користувачем рядок до 64 байт.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Встановлення клієнтської інформації**

```php
<?php

$c = oci_connect('hr', 'welcome', 'localhost/XE');

// Запись информации о клиенте
oci_set_client_info($c, 'My Application Version 2');

// Код, осуществляющий запрос к БД, например выборка:
$s = oci_parse($c, 'select * from dual');
oci_execute($s);
oci_fetch_all($s, $res);

sleep(30);

?>
```

```
// Пока скрипт выполняется, администратор может увидеть клиентскую
// информацию:

sqlplus system/welcome
SQL> select client_info from v$session;
```

### Примітки

> **Зауваження** **Вимога до версії Oracle**
> 
> Ця функція доступна, якщо PHP злінковано з бібліотеками Oracle Database починаючи з версії 10*г* і вище.

**Підказка**

# Продуктивність

У старих версіях OCI8 або бази даних Oracle можна було встановити інформацію про клієнта за допомогою пакета `DBMS_APPLICATION_INFO`. Для цієї мети ефективніше використання функції **ocisetclientinfo()**

**Застереження**

# Порада щодо повного сканування таблиці (roundtrip)

Деякі, але не всі функції OCI8 викликають повне сканування таблиці (roundtrip). Повне сканування таблиць немає для тих запитів, у яких включено кешування результатів у базі даних.

### Дивіться також

-   [oci\_set\_module\_name()](function.oci-set-module-name.html) - Задає ім'я модулю
-   [oci\_set\_action()](function.oci-set-action.html) - Вказує ім'я для дії
-   [oci\_set\_client\_identifier()](function.oci-set-client-identifier.html) - задає ідентифікатор клієнта
-   [oci\_set\_db\_operation()](function.oci-set-db-operation.html) - Задає операцію бази даних