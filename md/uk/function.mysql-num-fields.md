Повертає кількість полів результату запиту

-   [« mysqllisttables](function.mysql-list-tables.html)
    
-   [mysqlnumrows »](function.mysql-num-rows.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Повертає кількість полів результату запиту
    

# mysqlnumfields

(PHP 4, PHP 5)

mysqlnumfields — Повертає кількість полів результату запиту

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.html) або [PDOMySQL](ref.pdo-mysql.html). Дивіться також інструкцію [MySQL: выбор API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   [mysqlinumfields()](mysqli-result.field-count.html)
-   [PDOStatement::columnCount()](pdostatement.columncount.html)

### Опис

```methodsynopsis
mysql_num_fields(resource $result): int|false
```

Повертає кількість полів у результаті запиту.

### Список параметрів

`result`

оброблюваний [результат запроса](language.types.resource.html). Цей результат можна отримати за допомогою функції [mysqlquery()](function.mysql-query.html)

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

-   [mysqlselectdb()](function.mysql-select-db.html) - Вибирає базу даних MySQL
-   [mysqlquery()](function.mysql-query.html) - Надсилає запит MySQL
-   [mysqlfetchfield()](function.mysql-fetch-field.html) - Повертає інформацію про колонку з результату запиту як об'єкта
-   [mysqlnumrows()](function.mysql-num-rows.html) - Повертає кількість рядів результату запиту