---
navigation:
  - mongodb-driver-manager.getreadconcern.md: '« MongoDBDriverManager::getReadConcern'
  - mongodb-driver-manager.getservers.md: 'MongoDBDriverManager::getServers »'
  - index.md: PHP Manual
  - class.mongodb-driver-manager.md: MongoDBDriverManager
title: 'MongoDBDriverManager::getReadPreference'
---
# MongoDBDriverManager::getReadPreference

(mongodb >=1.0.0)

MongoDBDriverManager::getReadPreference — Повертає ReadPreference для Manager

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::getReadPreference(): MongoDB\Driver\ReadPreference
```

Повертає [MongoDBDriverReadPreference](class.mongodb-driver-readpreference.md) для Manager, отриманий із його URI-опцій. Це перевага для читання за промовчанням для запитів і команд, що виконуються в Manager.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDBDriverReadPreference](class.mongodb-driver-readpreference.md) для Manager.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverManager::getReadPreference()****

```php
<?php

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
var_dump($manager->getReadPreference());

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017/?readPreference=secondaryPreferred&readPreferenceTags=dc:ny,rack:1&readPreferenceTags=dc:ny&readPreferenceTags=');
var_dump($manager->getReadPreference());

?>
```

Результатом виконання цього прикладу буде щось подібне:

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

-   [MongoDBDriverReadPreference](class.mongodb-driver-readpreference.md)
-   [MongoDBDriverManager::construct()](mongodb-driver-manager.construct.md) - Створює новий Manager MongoDB
