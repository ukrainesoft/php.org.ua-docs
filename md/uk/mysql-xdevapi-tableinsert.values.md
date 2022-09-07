---
navigation:
  - mysql-xdevapi-tableinsert.execute.md: '« TableInsert::execute'
  - class.mysql-xdevapi-tableselect.md: mysqlxdevapiTableSelect »
  - index.md: PHP Manual
  - class.mysql-xdevapi-tableinsert.md: mysqlxdevapiTableInsert
title: 'TableInsert::values'
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

**Приклад #1 Приклад використання **mysqlxdevapiTableInsert::values()****

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
