Повертає тип вказаного поля з результату запиту

-   [« mysqlfieldtable](function.mysql-field-table.html)
    
-   [mysqlfreeresult »](function.mysql-free-result.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Повертає тип вказаного поля з результату запиту
    

# mysqlfieldtype

(PHP 4, PHP 5)

mysqlfieldtype — Повернення типу вказаного поля з результату запиту

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.html) або [PDOMySQL](ref.pdo-mysql.html). Дивіться також інструкцію [MySQL: выбор API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   [mysqlifetchfielddirect()](mysqli-result.fetch-field-direct.html) type
-   [PDOStatement::getColumnMeta()](pdostatement.getcolumnmeta.html) driver:decltype або pdotype

### Опис

```methodsynopsis
mysql_field_type(resource $result, int $field_offset): string
```

Функція **mysqlfieldtype()** аналогічна функції [mysqlfieldname()](function.mysql-field-name.html). Аргументи однакові, але замість імені колонки повертається її тип.

### Список параметрів

`result`

оброблюваний [результат запроса](language.types.resource.html). Цей результат можна отримати за допомогою функції [mysqlquery()](function.mysql-query.html)

`field_offset`

Числове усунення поля . `field_offset` починається з `0`. Якщо `field_offset` не існує, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Поля можуть бути такі типи: `"int"` `"real"` `"string"` `"blob"` та інших, докладно описаних [» документации MySQL](http://dev.mysql.com/doc/)

### Приклади

**Приклад #1 Приклад використання **mysqlfieldtype()****

```php
<?php
mysql_connect("localhost", "mysql_username", "mysql_password");
mysql_select_db("mysql");
$result = mysql_query("SELECT * FROM func");
$fields = mysql_num_fields($result);
$rows   = mysql_num_rows($result);
$table  = mysql_field_table($result, 0);
echo "Ваша таблица '" . $table . "' содержит " . $fields . " поля и " . $rows . " запись\n";
echo "В таблице есть следующие поля:\n";
for ($i=0; $i < $fields; $i++) {
    $type  = mysql_field_type($result, $i);
    $name  = mysql_field_name($result, $i);
    $len   = mysql_field_len($result, $i);
    $flags = mysql_field_flags($result, $i);
    echo $type . " " . $name . " " . $len . " " . $flags . "\n";
}
mysql_free_result($result);
mysql_close();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ваша таблица 'func' содержит 4 поля и 1 запись
В таблице есть следующие поля:
string name 64 not_null primary_key binary
int ret 1 not_null
string dl 128 not_null
string type 9 not_null enum
```

### Примітки

> **Зауваження**
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **mysqlfieldtype()**

### Дивіться також

-   [mysqlfieldname()](function.mysql-field-name.html) - Повертає назву вказаної колонки результату запиту
-   [mysqlfieldlen()](function.mysql-field-len.html) - Повертає довжину вказаного поля