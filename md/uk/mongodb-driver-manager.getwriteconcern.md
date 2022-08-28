Повертає WriteConcern для Manager

-   [« MongoDB\\Driver\\Manager::getServers](mongodb-driver-manager.getservers.html)
    
-   [MongoDB\\Driver\\Manager::removeSubscriber »](mongodb-driver-manager.removesubscriber.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Manager](class.mongodb-driver-manager.html)
    
-   Повертає WriteConcern для Manager
    

# MongoDBDriverManager::getWriteConcern

(mongodb >=1.0.0)

MongoDBDriverManager::getWriteConcern — Повертає WriteConcern для Manager

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::getWriteConcern(): MongoDB\Driver\WriteConcern
```

Повертає [MongoDB\\Driver\\WriteConcern](class.mongodb-driver-writeconcern.html) для Manager, отриманий із його URI-опцій. Це гарантія запису за промовчанням для запитів і команд, що виконуються в Manager.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

[MongoDB\\Driver\\WriteConcern](class.mongodb-driver-writeconcern.html) для Manager.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverManager::getWriteConcern()****

```php
<?php

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
var_dump($manager->getWriteConcern());

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017/?w=majority&wtimeoutMS=2000');
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

-   [MongoDB\\Driver\\WriteConcern](class.mongodb-driver-writeconcern.html)
-   [MongoDB\\Driver\\Manager::\_\_construct()](mongodb-driver-manager.construct.html) - Створює новий Manager MongoDB