---
navigation:
  - mysql-xdevapi-table.construct.md: '« Table::\_\_construct'
  - mysql-xdevapi-table.delete.md: 'Table::delete »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-table.md: mysql\_xdevapi\\Table
title: 'Table::count'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

**Пример #1 Пример использования**mysql\_xdevapi\\Table::count()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();
$session->sql("CREATE TABLE addressbook.names(name text, age int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 33)")->execute();

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

var_dump($table->count());
?>
```

Результат виконання наведеного прикладу:

```
int(2)
```
