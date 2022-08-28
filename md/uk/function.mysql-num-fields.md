Повертає кількість полів результату запиту

-   [« mysql\_list\_tables](function.mysql-list-tables.html)
    
-   [mysql\_num\_rows »](function.mysql-num-rows.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Повертає кількість полів результату запиту
    

# mysqlnumfields

(PHP 4, PHP 5)

mysqlnumfields — Повертає кількість полів результату запиту

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.html) або [PDO\_MySQL](ref.pdo-mysql.html). Дивіться також інструкцію [MySQL: выбор API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   [mysqli\_num\_fields()](mysqli-result.field-count.html)
-   [PDOStatement::columnCount()](pdostatement.columncount.html)

### Опис

```methodsynopsis
mysql_num_fields(resource $result): int|false
```

Повертає кількість полів у результаті запиту.

### Список параметрів

`result`

оброблюваний [результат запроса](language.types.resource.html). Цей результат можна отримати за допомогою функції [mysql\_query()](function.mysql-query.html)

### Значення, що повертаються

Повертає кількість полів у результаті запиту (resource) у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqlnumfields()****

```php
<?php
$result = mysql_query("SELECT id,email FROM people WHERE id = '42'");
if (!$result) {
    echo 'Не удалось выполнить запрос: ' . mysql_error();
    exit;
}

/* возвращает 2, так как id,email === двум полям */
echo mysql_num_fields($result);
?>
```

### Примітки

> **Зауваження**
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **mysqlnumfields()**

### Дивіться також

-   [mysql\_select\_db()](function.mysql-select-db.html) - Вибирає базу даних MySQL
-   [mysql\_query()](function.mysql-query.html) - Надсилає запит MySQL
-   [mysql\_fetch\_field()](function.mysql-fetch-field.html) - Повертає інформацію про колонку з результату запиту як об'єкта
-   [mysql\_num\_rows()](function.mysql-num-rows.html) - Повертає кількість рядів результату запиту