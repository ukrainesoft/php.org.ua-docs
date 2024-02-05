---
navigation:
  - function.mysql-fetch-field.md: « mysql\_fetch\_field
  - function.mysql-fetch-object.md: mysql\_fetch\_object »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_fetch\_lengths
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_fetch\_lengths

(PHP 4, PHP 5)

mysql\_fetch\_lengths - Повертає довжину кожного поля в результаті

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_fetch\_lengths()](mysqli-result.lengths.md)
-   [PDOStatement::getColumnMeta()](pdostatement.getcolumnmeta.md)

### Опис

```methodsynopsis
mysql_fetch_lengths(resource $result): array|false
```

Повертає масив довжин кожного поля, що міститься в останньому ряду результату, отриманому з MySQL.

**mysql\_fetch\_lengths()** повертає довжини кожного поля, що міститься в останньому ряду, обробленому функціями [mysql\_fetch\_row()](function.mysql-fetch-row.md) [mysql\_fetch\_assoc()](function.mysql-fetch-assoc.md) [mysql\_fetch\_array()](function.mysql-fetch-array.md) і [mysql\_fetch\_object()](function.mysql-fetch-object.md) у масиві, що починається з 0.

### Список параметрів

`result`

оброблюваний [результат запиту](language.types.resource.md). Цей результат можна отримати за допомогою функції [mysql\_query()](function.mysql-query.md)

### Значення, що повертаються

Масив (array) довжин у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** mysql\_fetch\_lengths()\*\*\*\*

```php
<?php
$result = mysql_query("SELECT id,email FROM people WHERE id = '42'");
if (!$result) {
    echo 'Ошибка выполнения запроса: ' . mysql_error();
    exit;
}
$row     = mysql_fetch_assoc($result);
$lengths = mysql_fetch_lengths($result);

print_r($row);
print_r($lengths);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [id] => 42
    [email] => user@example.com
)
Array
(
    [0] => 2
    [1] => 16
)
```

### Дивіться також

-   [mysql\_field\_len()](function.mysql-field-len.md) \- Повертає довжину вказаного поля
-   [mysql\_fetch\_row()](function.mysql-fetch-row.md) \- Обробляє ряд результату запиту та повертає масив із числовими індексами
-   [strlen()](function.strlen.md) \- Повертає довжину рядка
