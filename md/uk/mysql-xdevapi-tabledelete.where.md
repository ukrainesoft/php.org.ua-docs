---
navigation:
  - mysql-xdevapi-tabledelete.orderby.md: '« TableDelete::orderby'
  - class.mysql-xdevapi-tableinsert.md: mysql\_xdevapi\\TableInsert »
  - index.md: PHP Manual
  - class.mysql-xdevapi-tabledelete.md: mysql\_xdevapi\\TableDelete
title: 'TableDelete::where'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

**Пример #1 Пример использования**mysql\_xdevapi\\TableDelete::where()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$table->delete()
  ->where("id = :id")
  ->bind(['id' => 42])
  ->limit(1)
  ->execute();

?>
```
