---
navigation:
  - function.mysql-num-fields.md: « mysql\_num\_fields
  - function.mysql-pconnect.md: mysql\_pconnect »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_num\_rows
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_num\_rows

(PHP 4, PHP 5)

mysql\_num\_rows — Повертає кількість рядів результату запиту

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_num\_rows()](mysqli-result.num-rows.md)
-   [mysqli\_stmt\_num\_rows()](mysqli-stmt.num-rows.md)
-   [PDOStatement::rowCount()](pdostatement.rowcount.md)

### Опис

```methodsynopsis
mysql_num_rows(resource $result): int|false
```

Повертає кількість рядів результатів запиту. Ця команда працює лише із запитами SELECT або SHOW, які повертають актуальний результат запиту. Щоб отримати кількість рядів, оброблених функціями INSERT, UPDATE, REPLACE та DELETE, використовуйте функцію [mysql\_affected\_rows()](function.mysql-affected-rows.md)

### Список параметрів

`result`

оброблюваний [результат запиту](language.types.resource.md). Цей результат можна отримати за допомогою функції [mysql\_query()](function.mysql-query.md)

### Значення, що повертаються

Кількість рядів в результаті запиту у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** mysql\_num\_rows()\*\*\*\*

```php
<?php

$link = mysql_connect("localhost", "mysql_user", "mysql_password");
mysql_select_db("database", $link);

$result = mysql_query("SELECT * FROM table1", $link);
$num_rows = mysql_num_rows($result);

echo "Получено $num_rows рядов\n";

?>
```

### Примітки

> **Зауваження** :
> 
> При использовании[mysql\_unbuffered\_query()](function.mysql-unbuffered-query.md)функция**mysql\_num\_rows()** не поверне коректного значення доти, доки всі ряди не будуть отримані.

> **Зауваження** :
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **mysql\_numrows()**

### Дивіться також

-   [mysql\_affected\_rows()](function.mysql-affected-rows.md) \- Повертає кількість порушених минулою операцією рядів
-   [mysql\_connect()](function.mysql-connect.md) \- Відкриває з'єднання із сервером MySQL
-   [mysql\_data\_seek()](function.mysql-data-seek.md) \- Переміщує внутрішній покажчик у результаті запиту
-   [mysql\_select\_db()](function.mysql-select-db.md) \- Вибирає базу даних MySQL
-   [mysql\_query()](function.mysql-query.md) \- Надсилає запит MySQL
