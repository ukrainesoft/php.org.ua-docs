---
navigation:
  - mysql-xdevapi-table.count.md: '« Table::count'
  - mysql-xdevapi-table.existsindatabase.md: 'Table::existsInDatabase »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-table.md: mysqlxdevapiTable
title: 'Table::delete'
---
# Table::delete

(No version information available, might only be in Git)

Table::delete — Видалити рядки з таблиці

### Опис

```methodsynopsis
public mysql_xdevapi\Table::delete(): mysql_xdevapi\TableDelete
```

Видаляє рядки з таблиці.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт TableDelete; використовуйте метод execute() для виконання запиту delete

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiTable::delete()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();
$session->sql("CREATE TABLE addressbook.names(name text, age int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 33)")->execute();

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$table->delete()->where("name = :name")->orderby("age DESC")->limit(1)->bind(['name' => 'John'])->execute();
?>
```
