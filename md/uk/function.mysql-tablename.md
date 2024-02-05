---
navigation:
  - function.mysql-stat.md: « mysql\_stat
  - function.mysql-thread-id.md: mysql\_thread\_id »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_tablename
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_tablename

(PHP 4, PHP 5)

mysql\_tablename — Повертає ім'я таблиці, яка містить вказане поле

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   SQL запит:`SHOW TABLES`

### Опис

```methodsynopsis
mysql_tablename(resource $result, int $i): string|false
```

Повертає ім'я таблиці з `result`

Ця функція застаріла. Замість неї рекомендується використання [mysql\_query()](function.mysql-query.md) із SQL-запитом `SHOW TABLES [FROM db_name] [LIKE 'pattern']`

### Список параметрів

`result`

Дескриптор результату типу resource, отриманий із виклику [mysql\_list\_tables()](function.mysql-list-tables.md)

`i`

Цілочисельний індекс (номер ряду/таблиці)

### Значення, що повертаються

Ім'я таблиці у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

Используйте функцию**mysql\_tablename()** для роботи з результатом запиту або будь-яку іншу функцію, здатну це робити, наприклад, [mysql\_fetch\_array()](function.mysql-fetch-array.md)

### Приклади

**Приклад #1 Приклад використання** mysql\_tablename()\*\*\*\*

```php
<?php
mysql_connect("localhost", "mysql_user", "mysql_password");
$result = mysql_list_tables("mydb");
$num_rows = mysql_num_rows($result);
for ($i = 0; $i < $num_rows; $i++) {
    echo "Table: ", mysql_tablename($result, $i), "\n";
}

mysql_free_result($result);
?>
```

### Примітки

> **Зауваження** :
> 
> Для визначення кількості таблиць в результаті запиту можна використати функцію [mysql\_num\_rows()](function.mysql-num-rows.md)

### Дивіться також

-   [mysql\_list\_tables()](function.mysql-list-tables.md) \- Повертає список таблиць бази даних MySQL
-   [mysql\_field\_table()](function.mysql-field-table.md) \- Повертає назву таблиці, до якої належить зазначене поле
-   [mysql\_db\_name()](function.mysql-db-name.md) \- Повертає назву бази даних із виклику до mysql\_list\_dbs
