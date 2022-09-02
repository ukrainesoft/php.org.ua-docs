---
navigation:
  - mysql-xdevapi-tableupdate.set.md: '« TableUpdate::set'
  - class.mysql-xdevapi-warning.md: mysqlxdevapiWarning »
  - index.md: PHP Manual
  - class.mysql-xdevapi-tableupdate.md: mysqlxdevapiTableUpdate
title: 'TableUpdate::where'
---
# TableUpdate::where

(No version information available, might only be in Git)

TableUpdate::where — Встановлює фільтр пошуку

### Опис

```methodsynopsis
public mysql_xdevapi\TableUpdate::where(string $where_expr): mysql_xdevapi\TableUpdate
```

Встановлює умову пошуку фільтрації.

### Список параметрів

`where_expr`

Умова пошуку для фільтрації документів чи записів.

### Значення, що повертаються

Об'єкт TableUpdate.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiTableUpdate::where()****

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
