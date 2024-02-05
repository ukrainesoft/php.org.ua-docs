---
navigation:
  - mongodb-driver-manager.getservers.md: '« MongoDB\\Driver\\Manager::getServers'
  - mongodb-driver-manager.removesubscriber.md: 'MongoDB\\Driver\\Manager::removeSubscriber »'
  - index.md: PHP Manual
  - class.mongodb-driver-manager.md: MongoDB\\Driver\\Manager
title: 'MongoDB\\Driver\\Manager::getWriteConcern'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Manager::getWriteConcern

(mongodb >=1.0.0)

MongoDB\\Driver\\Manager::getWriteConcern — Повертає WriteConcern для Manager

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::getWriteConcern(): MongoDB\Driver\WriteConcern
```

Повертає [MongoDB\\Driver\\WriteConcern](class.mongodb-driver-writeconcern.md) для Manager, отриманий із його URI-опцій. Це гарантія запису за промовчанням для запитів і команд, що виконуються в Manager.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

[MongoDB\\Driver\\WriteConcern](class.mongodb-driver-writeconcern.md)для Manager.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання** MongoDB\\Driver\\Manager::getWriteConcern()\*\*\*\*

```php
<?php

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
var_dump($manager->getWriteConcern());

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017/?w=majority&wtimeoutMS=2000');
var_dump($manager->getWriteConcern());

?>
```

Висновок наведеного прикладу буде схожим на:

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

-   [MongoDB\\Driver\\WriteConcern](class.mongodb-driver-writeconcern.md)
-   [MongoDB\\Driver\\Manager::\_\_construct()](mongodb-driver-manager.construct.md) \- Створює новий Manager MongoDB
