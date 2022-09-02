---
navigation:
  - mysql-xdevapi-tabledelete.orderby.md: '« TableDelete::orderby'
  - class.mysql-xdevapi-tableinsert.md: mysqlxdevapiTableInsert »
  - index.md: PHP Manual
  - class.mysql-xdevapi-tabledelete.md: mysqlxdevapiTableDelete
title: 'TableDelete::where'
---
# TableDelete::where

(No version information available, might only be in Git)

TableDelete::where — Встановлює умову пошуку для видалення

### Опис

```methodsynopsis
public mysql_xdevapi\TableDelete::where(string $where_expr): mysql_xdevapi\TableDelete
```

Встановлює умову пошуку фільтрації.

### Список параметрів

`where_expr`

Визначає умову пошуку фільтрації документів або записів.

### Значення, що повертаються

Об'єкт TableDelete.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiTableDelete::where()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$table->delete()
  ->where("id = :id")
  ->bind(['id' => 42])
  ->limit(1)
  ->execute();

?>
```
