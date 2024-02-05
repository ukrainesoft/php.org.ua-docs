---
navigation:
  - function.mysql-field-seek.md: « mysql\_field\_seek
  - function.mysql-field-type.md: mysql\_field\_type »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_field\_table
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_field\_table

(PHP 4, PHP 5)

mysql\_field\_table — Повертає назву таблиці, якій належить вказане поле

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_fetch\_field\_direct()](mysqli-result.fetch-field-direct.md) \[table\]или\[orgtable\]
-   [PDOStatement::getColumnMeta()](pdostatement.getcolumnmeta.md) \[table\]

### Опис

```methodsynopsis
mysql_field_table(resource $result, int $field_offset): string
```

Повертає назву таблиці, до якої належить зазначене поле.

### Список параметрів

`result`

оброблюваний [результат запиту](language.types.resource.md). Цей результат можна отримати за допомогою функції [mysql\_query()](function.mysql-query.md)

`field_offset`

Числовое смещение поля`field_offset` починається з . Якщо `field_offset` не існує, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Ім'я таблиці у разі успішного виконання.

### Приклади

**Пример #1 Пример использования**mysql\_field\_table()\*\*\*\*

```php
<?php

$query = "SELECT account.*, country.* FROM account, country WHERE country.name = 'Portugal' AND account.country_id = country.id";

// получаем результат из базы данных
$result = mysql_query($query);

// выводит имя таблицы и имя поля
for ($i = 0; $i < mysql_num_fields($result); ++$i) {
    $table = mysql_field_table($result, $i);
    $field = mysql_field_name($result, $i);

    echo  "$table: $field\n";
}

?>
```

### Примітки

> **Зауваження** :
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **mysql\_fieldtable()**

### Дивіться також

-   [mysql\_list\_tables()](function.mysql-list-tables.md) \- Повертає список таблиць бази даних MySQL
