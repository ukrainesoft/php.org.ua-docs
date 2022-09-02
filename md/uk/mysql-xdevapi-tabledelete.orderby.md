---
navigation:
  - mysql-xdevapi-tabledelete.limit.md: '« TableDelete::limit'
  - mysql-xdevapi-tabledelete.where.md: 'TableDelete::where »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-tabledelete.md: mysqlxdevapiTableDelete
title: 'TableDelete::orderby'
---
# TableDelete::orderby

(No version information available, might only be in Git)

TableDelete::orderby — Встановлює критерії сортування видалення

### Опис

```methodsynopsis
public mysql_xdevapi\TableDelete::orderby(string $orderby_expr): mysql_xdevapi\TableDelete
```

Встановлює параметри порядку для набору результатів.

### Список параметрів

`orderby_expr`

Визначення сортування.

### Значення, що повертаються

Об'єкт TableDelete.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiTableDelete::orderBy()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$table->delete()
  ->where("age = :age")
  ->bind(['age' => 42])
  ->orderby("name DESC")
  ->limit(1)
  ->execute();

?>
```
