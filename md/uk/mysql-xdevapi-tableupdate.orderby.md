---
navigation:
  - mysql-xdevapi-tableupdate.limit.md: '« TableUpdate::limit'
  - mysql-xdevapi-tableupdate.set.md: 'TableUpdate::set »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-tableupdate.md: mysql\_xdevapi\\TableUpdate
title: 'TableUpdate::orderby'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# TableUpdate::orderby

(No version information available, might only be in Git)

TableUpdate::orderby — Встановлює критерії сортування

### Опис

```methodsynopsis
public mysql_xdevapi\TableUpdate::orderby(mixed $orderby_expr, mixed ...$orderby_exprs): mysql_xdevapi\TableUpdate
```

Встановлює критерії сортування.

### Список параметрів

`orderby_expr`

Вирази, що визначають порядок за критеріями. Може бути масивом з одним або декількома виразами чи рядком.

`orderby_exprs`

Додаткові параметри sort\_expr.

### Значення, що повертаються

Об'єкт TableUpdate.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\TableUpdate::orderby()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$res = $table->update()
  ->set('level', 3)
  ->where('age > 15 and age < 22')
  ->limit(4)
  ->orderby(['age asc','name desc'])
  ->execute();
?>
```
