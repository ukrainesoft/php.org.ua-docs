Повертає кількість рядів результату запиту

-   [« mysql\_num\_fields](function.mysql-num-fields.html)
    
-   [mysql\_pconnect »](function.mysql-pconnect.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Повертає кількість рядів результату запиту
    

# mysqlnumrows

(PHP 4, PHP 5)

mysqlnumrows — Повертає кількість рядів результату запиту

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.html) або [PDO\_MySQL](ref.pdo-mysql.html). Дивіться також інструкцію [MySQL: выбор API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   [mysqli\_num\_rows()](mysqli-result.num-rows.html)
-   [mysqli\_stmt\_num\_rows()](mysqli-stmt.num-rows.html)
-   [PDOStatement::rowCount()](pdostatement.rowcount.html)

### Опис

```methodsynopsis
mysql_num_rows(resource $result): int|false
```

Повертає кількість рядів результатів запиту. Ця команда працює тільки із запитами SELECT або SHOW, які повертають актуальний результат запиту. Щоб отримати кількість рядів, оброблених функціями INSERT, UPDATE, REPLACE та DELETE, використовуйте функцію [mysql\_affected\_rows()](function.mysql-affected-rows.html)

### Список параметрів

`result`

оброблюваний [результат запроса](language.types.resource.html). Цей результат можна отримати за допомогою функції [mysql\_query()](function.mysql-query.html)

### Значення, що повертаються

Кількість рядів в результаті запиту у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqlnumrows()****

```php
<?php

$link = mysql_connect("localhost", "mysql_user", "mysql_password");
mysql_select_db("database", $link);

$result = mysql_query("SELECT * FROM table1", $link);
$num_rows = mysql_num_rows($result);

echo "Получено $num_rows рядов\n";

?>
```

### Примітки

> **Зауваження**
> 
> При використанні [mysql\_unbuffered\_query()](function.mysql-unbuffered-query.html) функція **mysqlnumrows()** не поверне коректного значення доти, доки всі ряди не будуть отримані.

> **Зауваження**
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **mysqlnumrows()**

### Дивіться також

-   [mysql\_affected\_rows()](function.mysql-affected-rows.html) - Повертає кількість порушених минулою операцією рядів
-   [mysql\_connect()](function.mysql-connect.html) - Відкриває з'єднання із сервером MySQL
-   [mysql\_data\_seek()](function.mysql-data-seek.html) - Переміщує внутрішній покажчик у результаті запиту
-   [mysql\_select\_db()](function.mysql-select-db.html) - Вибирає базу даних MySQL
-   [mysql\_query()](function.mysql-query.html) - Надсилає запит MySQL