Повертає прапори, пов'язані із зазначеним полем результату запиту

-   [« mysql\_fetch\_row](function.mysql-fetch-row.html)
    
-   [mysql\_field\_len »](function.mysql-field-len.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Повертає прапори, пов'язані із зазначеним полем результату запиту
    

# mysqlfieldflags

(PHP 4, PHP 5)

mysqlfieldflags — Повертає прапори, пов'язані із зазначеним полем результату запиту

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.html) або [PDO\_MySQL](ref.pdo-mysql.html). Дивіться також інструкцію [MySQL: выбор API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   [mysqli\_fetch\_field\_direct()](mysqli-result.fetch-field-direct.html) flags
-   [PDOStatement::getColumnMeta()](pdostatement.getcolumnmeta.html) flags

### Опис

```methodsynopsis
mysql_field_flags(resource $result, int $field_offset): string|false
```

**mysqlfieldflags()** повертає прапори, пов'язані із зазначеним полем. Кожен прапор повертається як окреме слово, відокремлене від попереднього пропуску. Отримане значення можна розбити на масив, використовуючи функцію [explode()](function.explode.html)

### Список параметрів

`result`

оброблюваний [результат запроса](language.types.resource.html). Цей результат можна отримати за допомогою функції [mysql\_query()](function.mysql-query.html)

`field_offset`

Числове усунення поля . `field_offset` починається з `0`. Якщо `field_offset` не існує, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає рядок із прапорами, пов'язаними з результатом або **`false`** у разі виникнення помилки.

Повертаються такі прапори, якщо ваша версія MySQL їх підтримує: `"not_null"` `"primary_key"` `"unique_key"` `"multiple_key"` `"blob"` `"unsigned"` `"zerofill"` `"binary"` `"enum"` `"auto_increment"` і `"timestamp"`

### Приклади

**Приклад #1 Приклад використання **mysqlfieldflags()****

```php
<?php
$result = mysql_query("SELECT id,email FROM people WHERE id = '42'");
if (!$result) {
    echo 'Ошибка в запросе: ' . mysql_error();
    exit;
}
$flags = mysql_field_flags($result, 0);

echo $flags;
print_r(explode(' ', $flags));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
not_null primary_key auto_increment
Array
(
    [0] => not_null
    [1] => primary_key
    [2] => auto_increment
)
```

### Примітки

> **Зауваження**
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **mysqlfieldflags()**

### Дивіться також

-   [mysql\_field\_type()](function.mysql-field-type.html) - Повертає тип вказаного поля із результату запиту
-   [mysql\_field\_len()](function.mysql-field-len.html) - Повертає довжину вказаного поля