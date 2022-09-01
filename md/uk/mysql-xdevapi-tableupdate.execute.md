---
navigation:
  - mysql-xdevapi-tableupdate.construct.html: '« TableUpdate::construct'
  - mysql-xdevapi-tableupdate.limit.html: 'TableUpdate::limit »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-tableupdate.html: mysqlxdevapiTableUpdate
title: 'TableUpdate::execute'
---
# TableUpdate::execute

(No version information available, might only be in Git)

TableUpdate::execute — Виконує запит на оновлення

### Опис

```methodsynopsis
public mysql_xdevapi\TableUpdate::execute(): mysql_xdevapi\TableUpdate
```

Виконує затвердження оновлення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт TableUpdate.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiTableUpdate::execute()****

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
