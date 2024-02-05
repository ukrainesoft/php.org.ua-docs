---
navigation:
  - function.mysql-data-seek.md: « mysql\_data\_seek
  - function.mysql-db-query.md: mysql\_db\_query »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_db\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_db\_name

(PHP 4, PHP 5)

mysql\_db\_name — Повертає назву бази даних із виклику до [mysql\_list\_dbs()](function.mysql-list-dbs.md)

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   Запит: `SELECT DATABASE()`

### Опис

```methodsynopsis
mysql_db_name(resource $result, int $row, mixed $field = NULL): string
```

Повертає назву бази даних із виклику до [mysql\_list\_dbs()](function.mysql-list-dbs.md)

### Список параметрів

`result`

Дескриптор результату, отриманий із виклику [mysql\_list\_dbs()](function.mysql-list-dbs.md)

`row`

Індекс у результаті.

`field`

Ім'я поля.

### Значення, що повертаються

Повертає назву бази даних у разі успішного виконання, або \*\*`false`**в случае ошибки. В случае возврата**`false`\*\*используйте[mysql\_error()](function.mysql-error.md) визначення природи помилок.

### Приклади

**Приклад #1 Приклад використання** mysql\_db\_name()\*\*\*\*

```php
<?php
error_reporting(E_ALL);

$link = mysql_connect('dbhost', 'username', 'password');
$db_list = mysql_list_dbs($link);

$i = 0;
$cnt = mysql_num_rows($db_list);
while ($i < $cnt) {
    echo mysql_db_name($db_list, $i) . "\n";
    $i++;
}
?>
```

### Примітки

> **Зауваження** :
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **mysql\_dbname()**

### Дивіться також

-   [mysql\_list\_dbs()](function.mysql-list-dbs.md) \- Повертає список баз даних, доступних на сервері
-   [mysql\_tablename()](function.mysql-tablename.md) \- Повертає ім'я таблиці, що містить вказане поле
