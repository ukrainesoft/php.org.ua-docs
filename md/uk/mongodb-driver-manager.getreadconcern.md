---
navigation:
  - mongodb-driver-manager.getencryptedfieldsmap.md: '« MongoDBDriverManager::getEncryptedFieldsMap'
  - mongodb-driver-manager.getreadpreference.md: 'MongoDBDriverManager::getReadPreference »'
  - index.md: PHP Manual
  - class.mongodb-driver-manager.md: MongoDBDriverManager
title: 'MongoDBDriverManager::getReadConcern'
---
# MongoDBDriverManager::getReadConcern

(mongodb >=1.1.0)

MongoDBDriverManager::getReadConcern — Повертає ReadConcern для Manager

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::getReadConcern(): MongoDB\Driver\ReadConcern
```

Повертає [MongoDBDriverReadConcern](class.mongodb-driver-readconcern.md) для Manager, отриманий із його URI-опцій. Це гарантія прочитання за промовчанням для запитів і команд, що виконуються в Manager.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

[MongoDBDriverReadConcern](class.mongodb-driver-readconcern.md) для Manager.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverManager::getReadConcern()****

```php
<?php

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
var_dump($manager->getReadConcern());

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017/?readConcernLevel=local');
var_dump($manager->getReadConcern());

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(MongoDB\Driver\ReadConcern)#2 (0) {
}
object(MongoDB\Driver\ReadConcern)#1 (1) {
  ["level"]=>
  string(5) "local"
}
```

### Дивіться також

-   [MongoDBDriverReadConcern](class.mongodb-driver-readconcern.md)
-   [MongoDBDriverManager::construct()](mongodb-driver-manager.construct.md) - Створює новий Manager MongoDB
