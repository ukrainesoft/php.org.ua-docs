---
navigation:
  - function.mysql-field-table.md: « mysql\_field\_table
  - function.mysql-free-result.md: mysql\_free\_result »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_field\_type
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_field\_type

(PHP 4, PHP 5)

mysql\_field\_type — Повернення типу вказаного поля з результату запиту

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_fetch\_field\_direct()](mysqli-result.fetch-field-direct.md) \[type\]
-   [PDOStatement::getColumnMeta()](pdostatement.getcolumnmeta.md) \[driver:decl\_type\]или\[pdo\_type\]

### Опис

```methodsynopsis
mysql_field_type(resource $result, int $field_offset): string
```

Функция**mysql\_field\_type()** аналогічна функції [mysql\_field\_name()](function.mysql-field-name.md). Аргументи однакові, але замість імені колонки повертається її тип.

### Список параметрів

`result`

оброблюваний [результат запиту](language.types.resource.md). Цей результат можна отримати за допомогою функції [mysql\_query()](function.mysql-query.md)

`field_offset`

Числовое смещение поля`field_offset` починається з . Якщо `field_offset` не існує, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Поля можуть бути такі типи: `"int"` `"real"` `"string"` `"blob"` та інших, докладно описаних [» документації MySQL](http://dev.mysql.com/doc/)

### Приклади

**Приклад #1 Приклад використання** mysql\_field\_type()\*\*\*\*

```php
<?php
mysql_connect("localhost", "mysql_username", "mysql_password");
mysql_select_db("mysql");
$result = mysql_query("SELECT * FROM func");
$fields = mysql_num_fields($result);
$rows   = mysql_num_rows($result);
$table  = mysql_field_table($result, 0);
echo "Ваша таблица '" . $table . "' содержит " . $fields . " поля и " . $rows . " запись\n";
echo "В таблице есть следующие поля:\n";
for ($i=0; $i < $fields; $i++) {
    $type  = mysql_field_type($result, $i);
    $name  = mysql_field_name($result, $i);
    $len   = mysql_field_len($result, $i);
    $flags = mysql_field_flags($result, $i);
    echo $type . " " . $name . " " . $len . " " . $flags . "\n";
}
mysql_free_result($result);
mysql_close();
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ваша таблица 'func' содержит 4 поля и 1 запись
В таблице есть следующие поля:
string name 64 not_null primary_key binary
int ret 1 not_null
string dl 128 not_null
string type 9 not_null enum
```

### Примітки

> **Зауваження** :
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **mysql\_fieldtype()**

### Дивіться також

-   [mysql\_field\_name()](function.mysql-field-name.md) \- Повертає назву вказаної колонки результату запиту
-   [mysql\_field\_len()](function.mysql-field-len.md) \- Повертає довжину вказаного поля
