Повертає довжину кожного поля в результаті

-   [« mysql\_fetch\_field](function.mysql-fetch-field.html)
    
-   [mysql\_fetch\_object »](function.mysql-fetch-object.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Повертає довжину кожного поля в результаті
    

# mysqlfetchlengths

(PHP 4, PHP 5)

mysqlfetchlengths - Повертає довжину кожного поля в результаті

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.html) або [PDO\_MySQL](ref.pdo-mysql.html). Дивіться також інструкцію [MySQL: выбор API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   [mysqli\_fetch\_lengths()](mysqli-result.lengths.html)
-   [PDOStatement::getColumnMeta()](pdostatement.getcolumnmeta.html)

### Опис

```methodsynopsis
mysql_fetch_lengths(resource $result): array|false
```

Повертає масив довжин кожного поля, що міститься в останньому ряду результату, отриманому з MySQL.

**mysqlfetchlengths()** повертає довжини кожного поля, що міститься в останньому ряду, обробленому функціями [mysql\_fetch\_row()](function.mysql-fetch-row.html) [mysql\_fetch\_assoc()](function.mysql-fetch-assoc.html) [mysql\_fetch\_array()](function.mysql-fetch-array.html) і [mysql\_fetch\_object()](function.mysql-fetch-object.html) у масиві, що починається з 0.

### Список параметрів

`result`

оброблюваний [результат запроса](language.types.resource.html). Цей результат можна отримати за допомогою функції [mysql\_query()](function.mysql-query.html)

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

-   [mysql\_field\_len()](function.mysql-field-len.html) - Повертає довжину вказаного поля
-   [mysql\_fetch\_row()](function.mysql-fetch-row.html) - Обробляє ряд результату запиту та повертає масив із числовими індексами
-   [strlen()](function.strlen.html) - Повертає довжину рядка