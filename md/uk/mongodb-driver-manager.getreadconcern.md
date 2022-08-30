Повертає ReadConcern для Manager

-   [« MongoDBDriverManager::getEncryptedFieldsMap](mongodb-driver-manager.getencryptedfieldsmap.html)
    
-   [MongoDBDriverManager::getReadPreference »](mongodb-driver-manager.getreadpreference.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverManager](class.mongodb-driver-manager.html)
    
-   Повертає ReadConcern для Manager
    

# MongoDBDriverManager::getReadConcern

(mongodb >=1.1.0)

MongoDBDriverManager::getReadConcern — Повертає ReadConcern для Manager

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::getReadConcern(): MongoDB\Driver\ReadConcern
```

Повертає [MongoDBDriverReadConcern](class.mongodb-driver-readconcern.html) для Manager, отриманий із його URI-опцій. Це гарантія прочитання за промовчанням для запитів і команд, що виконуються в Manager.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

[MongoDBDriverReadConcern](class.mongodb-driver-readconcern.html) для Manager.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverManager::getReadConcern()****

```php
<?php

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
var_dump($manager->getReadConcern());

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017/?readConcernLevel=local');
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

-   [MongoDBDriverReadConcern](class.mongodb-driver-readconcern.html)
-   [MongoDBDriverManager::construct()](mongodb-driver-manager.construct.html) - Створює новий Manager MongoDB