---
navigation:
  - mongodb-driver-manager.getencryptedfieldsmap.md: '« MongoDB\\Driver\\Manager::getEncryptedFieldsMap'
  - mongodb-driver-manager.getreadpreference.md: 'MongoDB\\Driver\\Manager::getReadPreference »'
  - index.md: PHP Manual
  - class.mongodb-driver-manager.md: MongoDB\\Driver\\Manager
title: 'MongoDB\\Driver\\Manager::getReadConcern'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Manager::getReadConcern

(mongodb >=1.1.0)

MongoDB\\Driver\\Manager::getReadConcern — Повертає ReadConcern для Manager

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::getReadConcern(): MongoDB\Driver\ReadConcern
```

Повертає [MongoDB\\Driver\\ReadConcern](class.mongodb-driver-readconcern.md) для Manager, отриманий із його URI-опцій. Це гарантія прочитання за промовчанням для запитів і команд, що виконуються в Manager.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

[MongoDB\\Driver\\ReadConcern](class.mongodb-driver-readconcern.md)для Manager.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання** MongoDB\\Driver\\Manager::getReadConcern()\*\*\*\*

```php
<?php

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
var_dump($manager->getReadConcern());

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017/?readConcernLevel=local');
var_dump($manager->getReadConcern());

?>
```

Висновок наведеного прикладу буде схожим на:

```
object(MongoDB\Driver\ReadConcern)#2 (0) {
}
object(MongoDB\Driver\ReadConcern)#1 (1) {
  ["level"]=>
  string(5) "local"
}
```

### Дивіться також

-   [MongoDB\\Driver\\ReadConcern](class.mongodb-driver-readconcern.md)
-   [MongoDB\\Driver\\Manager::\_\_construct()](mongodb-driver-manager.construct.md) \- Створює новий Manager MongoDB
