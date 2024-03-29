---
navigation:
  - mysql-xdevapi-tableinsert.construct.md: '« TableInsert::\_\_construct'
  - mysql-xdevapi-tableinsert.values.md: 'TableInsert::values »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-tableinsert.md: mysql\_xdevapi\\TableInsert
title: 'TableInsert::execute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# TableInsert::execute

(No version information available, might only be in Git)

TableInsert::execute — Виконує запит на вставку

### Опис

```methodsynopsis
public mysql_xdevapi\TableInsert::execute(): mysql_xdevapi\Result
```

Виконує твердження.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт Result.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\TableInsert::execute()\*\*\*\*

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
