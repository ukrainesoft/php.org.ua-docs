---
navigation:
  - function.mysql-list-tables.md: « mysql\_list\_tables
  - function.mysql-num-rows.md: mysql\_num\_rows »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_num\_fields
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_num\_fields

(PHP 4, PHP 5)

mysql\_num\_fields — Повертає кількість полів результату запиту

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_num\_fields()](mysqli-result.field-count.md)
-   [PDOStatement::columnCount()](pdostatement.columncount.md)

### Опис

```methodsynopsis
mysql_num_fields(resource $result): int|false
```

Повертає кількість полів у результаті запиту.

### Список параметрів

`result`

оброблюваний [результат запиту](language.types.resource.md). Цей результат можна отримати за допомогою функції [mysql\_query()](function.mysql-query.md)

### Значення, що повертаються

Повертає кількість полів у результаті запиту (resource) у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**mysql\_num\_fields()\*\*\*\*

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

> **Зауваження** :
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **mysql\_numfields()**

### Дивіться також

-   [mysql\_select\_db()](function.mysql-select-db.md) \- Вибирає базу даних MySQL
-   [mysql\_query()](function.mysql-query.md) \- Надсилає запит MySQL
-   [mysql\_fetch\_field()](function.mysql-fetch-field.md) \- Повертає інформацію про колонку з результату запиту як об'єкта
-   [mysql\_num\_rows()](function.mysql-num-rows.md) \- Повертає кількість рядів результату запиту
