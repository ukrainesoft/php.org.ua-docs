---
navigation:
  - function.mysql-num-fields.html: « mysqlnumfields
  - function.mysql-pconnect.html: mysqlpconnect »
  - index.html: PHP Manual
  - ref.mysql.html: MySQL
title: mysqlnumrows
---
# mysqlnumrows

(PHP 4, PHP 5)

mysqlnumrows — Повертає кількість рядів результату запиту

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.html) або [PDOMySQL](ref.pdo-mysql.html). Дивіться також інструкцію [MySQL: вибір API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   [mysqlinumrows()](mysqli-result.num-rows.html)
-   [mysqlistmtnumrows()](mysqli-stmt.num-rows.html)
-   [PDOStatement::rowCount()](pdostatement.rowcount.html)

### Опис

```methodsynopsis
mysql_num_rows(resource $result): int|false
```

Повертає кількість рядів результатів запиту. Ця команда працює тільки із запитами SELECT або SHOW, які повертають актуальний результат запиту. Щоб отримати кількість рядів, оброблених функціями INSERT, UPDATE, REPLACE та DELETE, використовуйте функцію [mysqlaffectedrows()](function.mysql-affected-rows.html)

### Список параметрів

`result`

оброблюваний [результат запроса](language.types.resource.html). Цей результат можна отримати за допомогою функції [mysqlquery()](function.mysql-query.html)

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
> При використанні [mysqlunbufferedquery()](function.mysql-unbuffered-query.html) функція **mysqlnumrows()** не поверне коректного значення доти, доки всі ряди не будуть отримані.

> **Зауваження**
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **mysqlnumrows()**

### Дивіться також

-   [mysqlaffectedrows()](function.mysql-affected-rows.html) - Повертає кількість порушених минулою операцією рядів
-   [mysqlconnect()](function.mysql-connect.html) - Відкриває з'єднання із сервером MySQL
-   [mysqldataseek()](function.mysql-data-seek.html) - Переміщує внутрішній покажчик у результаті запиту
-   [mysqlselectdb()](function.mysql-select-db.html) - Вибирає базу даних MySQL
-   [mysqlquery()](function.mysql-query.html) - Надсилає запит MySQL
