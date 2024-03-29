---
navigation:
  - mysql-xdevapi-tabledelete.construct.md: '« TableDelete::\_\_construct'
  - mysql-xdevapi-tabledelete.limit.md: 'TableDelete::limit »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-tabledelete.md: mysql\_xdevapi\\TableDelete
title: 'TableDelete::execute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# TableDelete::execute

(No version information available, might only be in Git)

TableDelete::execute — Виконує запит на видалення

### Опис

```methodsynopsis
public mysql_xdevapi\TableDelete::execute(): mysql_xdevapi\Result
```

Виконує запит на видалення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт Result.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\TableDelete::execute()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();
$session->sql("CREATE TABLE addressbook.names(name text, age int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 33)")->execute();

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$table->delete()
  ->where("name = :name")
  ->bind(['name' => 'John'])
  ->orderby("age DESC")
  ->limit(1)
  ->execute();

?>
```
