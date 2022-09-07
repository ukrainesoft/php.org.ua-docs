---
navigation:
  - function.mysql-list-tables.md: « mysqllisttables
  - function.mysql-num-rows.md: mysqlnumrows »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysqlnumfields
---
# mysqlnumfields

(PHP 4, PHP 5)

mysqlnumfields — Повертає кількість полів результату запиту

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDOMySQL](ref.pdo-mysql.md). Дивіться також інструкцію [MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqlinumfields()](mysqli-result.field-count.md)
-   [PDOStatement::columnCount()](pdostatement.columncount.md)

### Опис

```methodsynopsis
mysql_num_fields(resource $result): int|false
```

Повертає кількість полів у результаті запиту.

### Список параметрів

`result`

оброблюваний [результат запроса](language.types.resource.md). Цей результат можна отримати за допомогою функції [mysqlquery()](function.mysql-query.md)

### Значення, що повертаються

Повертає кількість полів у результаті запиту (resource) у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqlnumfields()****

```php
<?php
$result = mysql_query("SELECT id,email FROM people WHERE id = '42'");
if (!$result) {
    echo 'Не удалось выполнить запрос: ' . mysql_error();
    exit;
}

/* возвращает 2, так как id,email === двум полям */
echo mysql_num_fields($result);
?>
```

### Примітки

> **Зауваження**
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **mysqlnumfields()**

### Дивіться також

-   [mysqlselectdb()](function.mysql-select-db.md) - Вибирає базу даних MySQL
-   [mysqlquery()](function.mysql-query.md) - Надсилає запит MySQL
-   [mysqlfetchfield()](function.mysql-fetch-field.md) - Повертає інформацію про колонку з результату запиту як об'єкта
-   [mysqlnumrows()](function.mysql-num-rows.md) - Повертає кількість рядів результату запиту
