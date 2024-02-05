---
navigation:
  - class.mysql-xdevapi-tableupdate.md: « mysql\_xdevapi\\TableUpdate
  - mysql-xdevapi-tableupdate.construct.md: 'TableUpdate::\_\_construct »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-tableupdate.md: mysql\_xdevapi\\TableUpdate
title: 'TableUpdate::bind'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# TableUpdate::bind

(No version information available, might only be in Git)

TableUpdate::bind — Прив'язує параметри запиту на оновлення

### Опис

```methodsynopsis
public mysql_xdevapi\TableUpdate::bind(array $placeholder_values): mysql_xdevapi\TableUpdate
```

Прив'язує значення до певного наповнювача.

### Список параметрів

`placeholder_values`

Ім'я заповнювача та значення для прив'язки, визначене як масив JSON.

### Значення, що повертаються

Об'єкт TableUpdate.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\TableUpdate::bind()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$table->update()
  ->set('status', 'admin')
  ->where('name = :name and age > :age')
  ->bind(['name' => 'Bernie', 'age' => 2000])
  ->execute();

?>
```
