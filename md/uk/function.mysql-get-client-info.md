Повертає дані про MySQL-клієнт

-   [« mysql\_free\_result](function.mysql-free-result.html)
    
-   [mysql\_get\_host\_info »](function.mysql-get-host-info.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Повертає дані про MySQL-клієнт
    

# mysqlgetclientinfo

(PHP 4> = 4.0.5, PHP 5)

mysqlgetclientinfo — Повертає дані про MySQL-клієнт

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.html) або [PDO\_MySQL](ref.pdo-mysql.html). Дивіться також інструкцію [MySQL: выбор API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   [mysqli\_get\_client\_info()](mysqli.get-client-info.html)
-   [PDO::getAttribute(PDO::ATTR\_CLIENT\_VERSION)](pdo.getattribute.html)

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
printf("Версия клиентской библиотеки MySQL: %s\n", mysql_get_client_info());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Версия клиентской библиотеки MySQL: 3.23.39
```

### Дивіться також

-   [mysql\_get\_host\_info()](function.mysql-get-host-info.html) - Повертає інформацію про з'єднання з MySQL
-   [mysql\_get\_proto\_info()](function.mysql-get-proto-info.html) - Повертає інформацію про протокол MySQL
-   [mysql\_get\_server\_info()](function.mysql-get-server-info.html) - Повертає інформацію про сервер MySQL