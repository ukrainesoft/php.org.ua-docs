---
navigation:
  - class.mysql-xdevapi-tableinsert.md: « mysql\_xdevapi\\TableInsert
  - mysql-xdevapi-tableinsert.execute.md: 'TableInsert::execute »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-tableinsert.md: mysql\_xdevapi\\TableInsert
title: 'TableInsert::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# TableInsert::\_\_construct

(No version information available, might only be in Git)

TableInsert::\_\_construct — Конструктор класу TableInsert

### Опис

private**mysql\_xdevapi\\TableInsert::\_\_construct**()

Ініціюється за допомогою методу insert().

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\TableInsert::\_\_construct()\*\*\*\*

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
