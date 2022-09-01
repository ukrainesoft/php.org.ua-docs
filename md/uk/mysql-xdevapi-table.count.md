---
navigation:
  - mysql-xdevapi-table.construct.html: '« Table::construct'
  - mysql-xdevapi-table.delete.html: 'Table::delete »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-table.html: mysqlxdevapiTable
title: 'Table::count'
---
# Table::count

(No version information available, might only be in Git)

Table::count — Отримати кількість рядків

### Опис

```methodsynopsis
public mysql_xdevapi\Table::count(): int
```

Отримати кількість рядків у таблиці.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Загальна кількість рядків у таблиці.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiTable::count()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();
$session->sql("CREATE TABLE addressbook.names(name text, age int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 33)")->execute();

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

var_dump($table->count());
?>
```

Результат виконання цього прикладу:

```
int(2)
```
