---
navigation:
  - mysql-xdevapi-table.getname.md: '« Table::getName'
  - mysql-xdevapi-table.getsession.md: 'Table::getSession »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-table.md: mysql\_xdevapi\\Table
title: 'Table::getSchema'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Table::getSchema

(No version information available, might only be in Git)

Table::getSchema — Отримати схему таблиці

### Опис

```methodsynopsis
public mysql_xdevapi\Table::getSchema(): mysql_xdevapi\Schema
```

Витягти схему, пов'язану з таблицею.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт Schema.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\Table::getSchema()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();
$session->sql("CREATE TABLE addressbook.names(name text, age int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 33)")->execute();

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

var_dump($table->getSchema());
?>
```

Висновок наведеного прикладу буде схожим на:

```
object(mysql_xdevapi\Schema)#9 (1) {
  ["name"]=>
  string(11) "addressbook"
}
```
