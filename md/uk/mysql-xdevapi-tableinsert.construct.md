---
navigation:
  - class.mysql-xdevapi-tableinsert.md: « mysqlxdevapiTableInsert
  - mysql-xdevapi-tableinsert.execute.md: 'TableInsert::execute »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-tableinsert.md: mysqlxdevapiTableInsert
title: 'TableInsert::construct'
---
# TableInsert::construct

(No version information available, might only be in Git)

TableInsert::construct — Конструктор класу TableInsert

### Опис

private **mysqlxdevapiTableInsert::construct**

Ініціюється за допомогою методу insert().

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiTableInsert::construct()****

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
