---
navigation:
  - class.mysql-xdevapi-table.md: « mysql\_xdevapi\\Table
  - mysql-xdevapi-table.count.md: 'Table::count »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-table.md: mysql\_xdevapi\\Table
title: 'Table::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Table::\_\_construct

(No version information available, might only be in Git)

Table::\_\_construct — Конструктор Table

### Опис

private**mysql\_xdevapi\\Table::\_\_construct**()

Створити об'єкти таблиці.

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\Table::\_\_construct()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");
?>
```
