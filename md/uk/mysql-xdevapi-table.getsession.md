---
navigation:
  - mysql-xdevapi-table.getschema.md: '« Table::getSchema'
  - mysql-xdevapi-table.insert.md: 'Table::insert »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-table.md: mysql\_xdevapi\\Table
title: 'Table::getSession'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Table::getSession

(No version information available, might only be in Git)

Table::getSession — Отримати таблицю сесій

### Опис

```methodsynopsis
public mysql_xdevapi\Table::getSession(): mysql_xdevapi\Session
```

Отримати сесію, пов'язану з таблицею.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт Session.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\Table::getSession()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();
$session->sql("CREATE TABLE addressbook.names(name text, age int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 33)")->execute();

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

var_dump($table->getSession());
?>
```

Висновок наведеного прикладу буде схожим на:

```
object(mysql_xdevapi\Session)#9 (0) {
}
```
