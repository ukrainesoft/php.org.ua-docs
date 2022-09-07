---
navigation:
  - mongodb-driver-manager.getservers.md: '« MongoDBDriverManager::getServers'
  - mongodb-driver-manager.removesubscriber.md: 'MongoDBDriverManager::removeSubscriber »'
  - index.md: PHP Manual
  - class.mongodb-driver-manager.md: MongoDBDriverManager
title: 'MongoDBDriverManager::getWriteConcern'
---
# MongoDBDriverManager::getWriteConcern

(mongodb >=1.0.0)

MongoDBDriverManager::getWriteConcern — Повертає WriteConcern для Manager

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::getWriteConcern(): MongoDB\Driver\WriteConcern
```

Повертає [MongoDBDriverWriteConcern](class.mongodb-driver-writeconcern.md) для Manager, отриманий із його URI-опцій. Це гарантія запису за промовчанням для запитів і команд, що виконуються в Manager.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

[MongoDBDriverWriteConcern](class.mongodb-driver-writeconcern.md) для Manager.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverManager::getWriteConcern()****

```php
<?php

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
var_dump($manager->getWriteConcern());

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017/?w=majority&wtimeoutMS=2000');
var_dump($manager->getWriteConcern());

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(MongoDB\Driver\WriteConcern)#2 (0) {
}
object(MongoDB\Driver\WriteConcern)#1 (2) {
  ["w"]=>
  string(8) "majority"
  ["wtimeout"]=>
  int(2000)
}
```

### Дивіться також

-   [MongoDBDriverWriteConcern](class.mongodb-driver-writeconcern.md)
-   [MongoDBDriverManager::construct()](mongodb-driver-manager.construct.md) - Створює новий Manager MongoDB
