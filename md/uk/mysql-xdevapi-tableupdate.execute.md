---
navigation:
  - mysql-xdevapi-tableupdate.construct.md: '« TableUpdate::\_\_construct'
  - mysql-xdevapi-tableupdate.limit.md: 'TableUpdate::limit »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-tableupdate.md: mysql\_xdevapi\\TableUpdate
title: 'TableUpdate::execute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

**Пример #1 Пример использования**mysql\_xdevapi\\TableUpdate::execute()\*\*\*\*

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
