---
navigation:
  - mysql-xdevapi-tabledelete.bind.md: '« TableDelete::bind'
  - mysql-xdevapi-tabledelete.execute.md: 'TableDelete::execute »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-tabledelete.md: mysql\_xdevapi\\TableDelete
title: 'TableDelete::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# TableDelete::\_\_construct

(No version information available, might only be in Git)

TableDelete::\_\_construct - Конструктор класу TableDelete

### Опис

private **mysql\_xdevapi\\TableDelete::\_\_construct**()

Ініціюється за допомогою методу delete().

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\TableDelete::\_\_construct()\*\*\*\*

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
