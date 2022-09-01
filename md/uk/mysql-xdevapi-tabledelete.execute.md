---
navigation:
  - mysql-xdevapi-tabledelete.construct.html: '« TableDelete::construct'
  - mysql-xdevapi-tabledelete.limit.html: 'TableDelete::limit »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-tabledelete.html: mysqlxdevapiTableDelete
title: 'TableDelete::execute'
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

**Приклад #1 Приклад використання **mysqlxdevapiTableDelete::execute()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();
$session->sql("CREATE TABLE addressbook.names(name text, age int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 33)")->execute();

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$table->delete()
  ->where("name = :name")
  ->bind(['name' => 'John'])
  ->orderby("age DESC")
  ->limit(1)
  ->execute();

?>
```
