---
navigation:
  - mysql-xdevapi-tableupdate.bind.md: '« TableUpdate::bind'
  - mysql-xdevapi-tableupdate.execute.md: 'TableUpdate::execute »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-tableupdate.md: mysql\_xdevapi\\TableUpdate
title: 'TableUpdate::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# TableUpdate::\_\_construct

(No version information available, might only be in Git)

TableUpdate::\_\_construct - Конструктор класу TableUpdate

### Опис

private**mysql\_xdevapi\\TableUpdate::\_\_construct**()

Ініціюється за допомогою методу update().

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\TableUpdate::\_\_construct()\*\*\*\*

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
