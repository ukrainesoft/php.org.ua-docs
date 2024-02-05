---
navigation:
  - mysql-xdevapi-table.existsindatabase.md: '« Table::existsInDatabase'
  - mysql-xdevapi-table.getschema.md: 'Table::getSchema »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-table.md: mysql\_xdevapi\\Table
title: 'Table::getName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Table::getName

(No version information available, might only be in Git)

Table::getName — Отримати ім'я таблиці

### Опис

```methodsynopsis
public mysql_xdevapi\Table::getName(): string
```

Повертає ім'я бази даних.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Назва об'єкта бази даних.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\Table::getName()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();
$session->sql("CREATE TABLE addressbook.names(name text, age int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 33)")->execute();

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

var_dump($table->getName());
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(5) "names"
```
