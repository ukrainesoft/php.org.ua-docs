---
navigation:
  - function.mysql-fetch-field.html: « mysqlfetchfield
  - function.mysql-fetch-object.html: mysqlfetchobject »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysqlfetchlengths
---
# mysqlfetchlengths

(PHP 4, PHP 5)

mysqlfetchlengths - Повертає довжину кожного поля в результаті

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDOMySQL](ref.pdo-mysql.md). Дивіться також інструкцію [MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqlifetchlengths()](mysqli-result.lengths.md)
-   [PDOStatement::getColumnMeta()](pdostatement.getcolumnmeta.md)

### Опис

```methodsynopsis
mysql_fetch_lengths(resource $result): array|false
```

Повертає масив довжин кожного поля, що міститься в останньому ряду результату, отриманому з MySQL.

**mysqlfetchlengths()** повертає довжини кожного поля, що міститься в останньому ряду, обробленому функціями [mysqlfetchrow()](function.mysql-fetch-row.html) [mysqlfetchassoc()](function.mysql-fetch-assoc.html) [mysqlfetcharray()](function.mysql-fetch-array.html) і [mysqlfetchobject()](function.mysql-fetch-object.md) у масиві, що починається з 0.

### Список параметрів

`result`

оброблюваний [результат запроса](language.types.resource.md). Цей результат можна отримати за допомогою функції [mysqlquery()](function.mysql-query.md)

### Значення, що повертаються

Масив (array) довжин у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqlfetchlengths()****

```php
<?php
$result = mysql_query("SELECT id,email FROM people WHERE id = '42'");
if (!$result) {
    echo 'Ошибка выполнения запроса: ' . mysql_error();
    exit;
}
$row     = mysql_fetch_assoc($result);
$lengths = mysql_fetch_lengths($result);

print_r($row);
print_r($lengths);
?>
```

Результатом виконання цього прикладу буде щось подібне:

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

-   [mysqlfieldlen()](function.mysql-field-len.md) - Повертає довжину вказаного поля
-   [mysqlfetchrow()](function.mysql-fetch-row.md) - Обробляє ряд результату запиту та повертає масив із числовими індексами
-   [strlen()](function.strlen.md) - Повертає довжину рядка
