---
navigation:
  - mongodb-driver-manager.getreadconcern.md: '« MongoDB\\Driver\\Manager::getReadConcern'
  - mongodb-driver-manager.getservers.md: 'MongoDB\\Driver\\Manager::getServers »'
  - index.md: PHP Manual
  - class.mongodb-driver-manager.md: MongoDB\\Driver\\Manager
title: 'MongoDB\\Driver\\Manager::getReadPreference'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Manager::getReadPreference

(mongodb >=1.0.0)

MongoDB\\Driver\\Manager::getReadPreference — Повертає ReadPreference для Manager

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::getReadPreference(): MongoDB\Driver\ReadPreference
```

Повертає [MongoDB\\Driver\\ReadPreference](class.mongodb-driver-readpreference.md) для Manager, отриманий із його URI-опцій. Це перевага для читання за промовчанням для запитів і команд, що виконуються в Manager.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDB\\Driver\\ReadPreference](class.mongodb-driver-readpreference.md)для Manager.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Пример #1 Пример использования**MongoDB\\Driver\\Manager::getReadPreference()\*\*\*\*

```php
<?php

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
var_dump($manager->getReadPreference());

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017/?readPreference=secondaryPreferred&readPreferenceTags=dc:ny,rack:1&readPreferenceTags=dc:ny&readPreferenceTags=');
var_dump($manager->getReadPreference());

?>
```

Висновок наведеного прикладу буде схожим на:

```
object(MongoDB\Driver\ReadPreference)#2 (1) {
  ["mode"]=>
  string(7) "primary"
}
object(MongoDB\Driver\ReadPreference)#1 (2) {
  ["mode"]=>
  string(18) "secondaryPreferred"
  ["tags"]=>
  array(3) {
    [0]=>
    object(stdClass)#3 (2) {
      ["dc"]=>
      string(2) "ny"
      ["rack"]=>
      string(1) "1"
    }
    [1]=>
    object(stdClass)#4 (1) {
      ["dc"]=>
      string(2) "ny"
    }
    [2]=>
    object(stdClass)#5 (0) {
    }
  }
}
```

### Дивіться також

-   [MongoDB\\Driver\\ReadPreference](class.mongodb-driver-readpreference.md)
-   [MongoDB\\Driver\\Manager::\_\_construct()](mongodb-driver-manager.construct.md) \- Створює новий Manager MongoDB
