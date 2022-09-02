---
navigation:
  - mysql-xdevapi-tableupdate.bind.md: '« TableUpdate::bind'
  - mysql-xdevapi-tableupdate.execute.md: 'TableUpdate::execute »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-tableupdate.md: mysqlxdevapiTableUpdate
title: 'TableUpdate::construct'
---
# TableUpdate::construct

(No version information available, might only be in Git)

TableUpdate::construct - Конструктор класу TableUpdate

### Опис

private **mysqlxdevapiTableUpdate::construct**

Ініціюється за допомогою методу update().

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiTableUpdate::construct()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$res = $table->update()
  ->set('level', 3)
  ->where('age > 15 and age < 22')
  ->limit(4)
  ->orderby(['age asc','name desc'])
  ->execute();

?>
```
