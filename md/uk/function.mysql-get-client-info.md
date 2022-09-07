---
navigation:
  - function.mysql-free-result.md: « mysqlfreeresult
  - function.mysql-get-host-info.md: mysqlgethostinfo »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysqlgetclientinfo
---
# mysqlgetclientinfo

(PHP 4> = 4.0.5, PHP 5)

mysqlgetclientinfo — Повертає дані про MySQL-клієнт

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDOMySQL](ref.pdo-mysql.md). Дивіться також інструкцію [MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqligetclientinfo()](mysqli.get-client-info.md)
-   [PDO::getAttribute(PDO::ATTRCLIENTVERSION)](pdo.getattribute.md)

### Опис

```methodsynopsis
mysql_get_client_info(): string
```

**mysqlgetclientinfo()** повертає рядок, який містить версію клієнтської бібліотеки.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Версія клієнтської бібліотеки MySQL

### Приклади

**Приклад #1 Приклад використання **mysqlgetclientinfo()****

```php
<?php
printf("Версия клиентской библиотеки MySQL: %s\n", mysql_get_client_info());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Версия клиентской библиотеки MySQL: 3.23.39
```

### Дивіться також

-   [mysqlgethostinfo()](function.mysql-get-host-info.md) - Повертає інформацію про з'єднання з MySQL
-   [mysqlgetprotoinfo()](function.mysql-get-proto-info.md) - Повертає інформацію про протокол MySQL
-   [mysqlgetserverinfo()](function.mysql-get-server-info.md) - Повертає інформацію про сервер MySQL
