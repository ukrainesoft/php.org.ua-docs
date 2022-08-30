Повертає назву таблиці, якій належить зазначене поле

-   [« mysqlfieldseek](function.mysql-field-seek.html)
    
-   [mysqlfieldtype »](function.mysql-field-type.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Повертає назву таблиці, якій належить зазначене поле
    

# mysqlfieldtable

(PHP 4, PHP 5)

mysqlfieldtable — Повертає назву таблиці, якій належить вказане поле

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.html) або [PDOMySQL](ref.pdo-mysql.html). Дивіться також інструкцію [MySQL: выбор API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   [mysqlifetchfielddirect()](mysqli-result.fetch-field-direct.html) table або orgtable
-   [PDOStatement::getColumnMeta()](pdostatement.getcolumnmeta.html) table

### Опис

```methodsynopsis
mysql_field_table(resource $result, int $field_offset): string
```

Повертає назву таблиці, до якої належить зазначене поле.

### Список параметрів

`result`

оброблюваний [результат запроса](language.types.resource.html). Цей результат можна отримати за допомогою функції [mysqlquery()](function.mysql-query.html)

`field_offset`

Числове усунення поля . `field_offset` починається з `0`. Якщо `field_offset` не існує, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Ім'я таблиці у разі успішного виконання.

### Приклади

**Приклад #1 Приклад використання **mysqlfieldtable()****

```php
<?php

$query = "SELECT account.*, country.* FROM account, country WHERE country.name = 'Portugal' AND account.country_id = country.id";

// получаем результат из базы данных
$result = mysql_query($query);

// выводит имя таблицы и имя поля
for ($i = 0; $i < mysql_num_fields($result); ++$i) {
    $table = mysql_field_table($result, $i);
    $field = mysql_field_name($result, $i);

    echo  "$table: $field\n";
}

?>
```

### Примітки

> **Зауваження**
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **mysqlfieldtable()**

### Дивіться також

-   [mysqllisttables()](function.mysql-list-tables.html) - Повертає список таблиць бази даних MySQL