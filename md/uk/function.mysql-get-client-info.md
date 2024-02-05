---
navigation:
  - function.mysql-free-result.md: « mysql\_free\_result
  - function.mysql-get-host-info.md: mysql\_get\_host\_info »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_get\_client\_info
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_get\_client\_info

(PHP 4 >= 4.0.5, PHP 5)

mysql\_get\_client\_info — Повертає дані про MySQL-клієнт

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_get\_client\_info()](mysqli.get-client-info.md)
-   [PDO::getAttribute()](pdo.getattribute.md)с параметром`attribute`заданим як\*\*`PDO::ATTR_CLIENT_VERSION`\*\*

### Опис

```methodsynopsis
mysql_get_client_info(): string
```

**mysql\_get\_client\_info()** повертає рядок, який містить версію клієнтської бібліотеки.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Версія клієнтської бібліотеки MySQL

### Приклади

**Приклад #1 Приклад використання** mysql\_get\_client\_info()\*\*\*\*

```php
<?php
printf("Версия клиентской библиотеки MySQL: %s\n", mysql_get_client_info());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Версия клиентской библиотеки MySQL: 3.23.39
```

### Дивіться також

-   [mysql\_get\_host\_info()](function.mysql-get-host-info.md) \- Повертає інформацію про з'єднання з MySQL
-   [mysql\_get\_proto\_info()](function.mysql-get-proto-info.md) \- Повертає інформацію про протокол MySQL
-   [mysql\_get\_server\_info()](function.mysql-get-server-info.md) \- Повертає інформацію про сервер MySQL
