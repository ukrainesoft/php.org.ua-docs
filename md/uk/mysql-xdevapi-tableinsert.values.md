---
navigation:
  - mysql-xdevapi-tableinsert.execute.md: '« TableInsert::execute'
  - class.mysql-xdevapi-tableselect.md: mysql\_xdevapi\\TableSelect »
  - index.md: PHP Manual
  - class.mysql-xdevapi-tableinsert.md: mysql\_xdevapi\\TableInsert
title: 'TableInsert::values'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# TableInsert::values

(No version information available, might only be in Git)

TableInsert::values ​​— Додає значення вставки рядка

### Опис

```methodsynopsis
public mysql_xdevapi\TableInsert::values(array $row_values): mysql_xdevapi\TableInsert
```

Встановлює значення для вставки.

### Список параметрів

`row_values`

Значення (масив) шпальт для вставки.

### Значення, що повертаються

Об'єкт TableInsert.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\TableInsert::values()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();
$session->sql("CREATE TABLE addressbook.names(name text, age int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 33)")->execute();

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$table
  ->insert("name", "age")
  ->values(["Suzanne", 31],["Julie", 43])
  ->execute();
?>
```
