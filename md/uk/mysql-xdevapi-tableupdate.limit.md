---
navigation:
  - mysql-xdevapi-tableupdate.execute.md: '« TableUpdate::execute'
  - mysql-xdevapi-tableupdate.orderby.md: 'TableUpdate::orderby »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-tableupdate.md: mysql\_xdevapi\\TableUpdate
title: 'TableUpdate::limit'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# TableUpdate::limit

(No version information available, might only be in Git)

TableUpdate::limit — Обмежує кількість рядків для оновлення

### Опис

```methodsynopsis
public mysql_xdevapi\TableUpdate::limit(int $rows): mysql_xdevapi\TableUpdate
```

Встановлює максимальну кількість записів або документів поновлення.

### Список параметрів

`rows`

Максимальна кількість записів чи документів для оновлення.

### Значення, що повертаються

Об'єкт TableUpdate.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\TableUpdate::limit()\*\*\*\*

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
