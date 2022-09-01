---
navigation:
  - class.mysql-xdevapi-tabledelete.html: « mysqlxdevapiTableDelete
  - mysql-xdevapi-tabledelete.construct.html: 'TableDelete::construct »'
  - index.html: PHP Manual
  - class.mysql-xdevapi-tabledelete.html: mysqlxdevapiTableDelete
title: 'TableDelete::bind'
---
# TableDelete::bind

(No version information available, might only be in Git)

TableDelete::bind — Зв'язує параметри запиту видалення

### Опис

```methodsynopsis
public mysql_xdevapi\TableDelete::bind(array $placeholder_values): mysql_xdevapi\TableDelete
```

Прив'язує значення до певного наповнювача.

### Список параметрів

`placeholder_values`

Ім'я заповнювача та значення для прив'язки.

### Значення, що повертаються

Об'єкт TableDelete.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiTableDelete::bind()****

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
