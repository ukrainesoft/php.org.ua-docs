---
navigation:
  - mysql-xdevapi-collectionremove.bind.md: '« CollectionRemove::bind'
  - mysql-xdevapi-collectionremove.execute.md: 'CollectionRemove::execute »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionremove.md: mysql\_xdevapi\\CollectionRemove
title: 'CollectionRemove::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CollectionRemove::\_\_construct

(No version information available, might only be in Git)

CollectionRemove::\_\_construct — Конструктор класу CollectionRemove

### Опис

private **mysql\_xdevapi\\CollectionRemove::\_\_construct**()

Видаляє документи колекції та створюється екземпляром методу **mysql\_xdevapi\\Collection::remove()**

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\Collection::remove()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema     = $session->getSchema("addressbook");
$collection = $schema->createCollection("people");

$collection->add('{"name": "Alfred", "age": 18, "job": "Butler"}')->execute();
$collection->add('{"name": "Bob",    "age": 19, "job": "Painter"}')->execute();

// Удаление всех художников
$collection
  ->remove("job in ('Painter')")
  ->execute();

// Удалить самого старого дворецкого
$collection
  ->remove("job in ('Butler')")
  ->sort('age desc')
  ->limit(1)
  ->execute();

// Удалить запись с самым низким возрастом
$collection
  ->remove('true')
  ->sort('age desc')
  ->limit(1)
  ->execute();
?>
```
