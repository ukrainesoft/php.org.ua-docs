---
navigation:
  - mysql-xdevapi-table.getsession.md: '« Table::getSession'
  - mysql-xdevapi-table.isview.md: 'Table::isView »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-table.md: mysql\_xdevapi\\Table
title: 'Table::insert'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Table::insert

(No version information available, might only be in Git)

Table::insert — Вставити рядки таблиці

### Опис

```methodsynopsis
public mysql_xdevapi\Table::insert(mixed $columns, mixed ...$more_columns): mysql_xdevapi\TableInsert
```

Вставляє рядки у таблицю.

### Список параметрів

`columns`

Стовпчики для вставки даних. Може бути масивом з одним або декількома значеннями або рядком.

`more_columns`

Визначення додаткових стовпців.

### Значення, що повертаються

Об'єкт TableInsert; використовуйте метод execute() для виконання виразу insert.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\Table::insert()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();
$session->sql("CREATE TABLE addressbook.names(name text, age int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 33)")->execute();

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$table ->insert("name", "age")
  ->values(["Suzanne", 31],["Julie", 43])
  ->execute();
?>
```
