---
navigation:
  - mysql-xdevapi-tableupdate.orderby.html: '« TableUpdate::orderby'
  - mysql-xdevapi-tableupdate.where.html: 'TableUpdate::where »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-tableupdate.html: mysqlxdevapiTableUpdate
title: 'TableUpdate::set'
---
# TableUpdate::set

(No version information available, might only be in Git)

TableUpdate::set — Додає поле для оновлення

### Опис

```methodsynopsis
public mysql_xdevapi\TableUpdate::set(string $table_field, string $expression_or_literal): mysql_xdevapi\TableUpdate
```

Оновлює значення стовпця для записів у таблиці.

### Список параметрів

`table_field`

Ім'я стовпця, що підлягає оновленню.

`expression_or_literal`

Значення, яке буде встановлене у вказаному стовпці.

### Значення, що повертаються

Об'єкт TableUpdate.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiTableUpdate::set()****

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
