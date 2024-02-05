---
navigation:
  - mysql-xdevapi-table.select.md: '« Table::select'
  - class.mysql-xdevapi-tabledelete.md: mysql\_xdevapi\\TableDelete »
  - index.md: PHP Manual
  - class.mysql-xdevapi-table.md: mysql\_xdevapi\\Table
title: 'Table::update'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Table::update

(No version information available, might only be in Git)

Table::update — Оновити рядки у таблиці

### Опис

```methodsynopsis
public mysql_xdevapi\Table::update(): mysql_xdevapi\TableUpdate
```

Оновлює стовпці у таблиці.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт TableUpdate; використовуйте метод execute() для виконання виразу update.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\Table::update()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();
$session->sql("CREATE TABLE addressbook.names(name text, age int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 33)")->execute();

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$table->update()->set('age',34)->where('name = "Sam"')->limit(1)->execute();
?>
```
