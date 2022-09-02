---
navigation:
  - mongodb-driver-manager.getreadpreference.md: '« MongoDBDriverManager::getReadPreference'
  - mongodb-driver-manager.getwriteconcern.md: 'MongoDBDriverManager::getWriteConcern »'
  - index.md: PHP Manual
  - class.mongodb-driver-manager.md: MongoDBDriverManager
title: 'MongoDBDriverManager::getServers'
---
# MongoDBDriverManager::getServers

(mongodb >=1.0.0)

MongoDBDriverManager::getServers — Повертає сервери, до яких підключено менеджера

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::getServers(): array
```

Повертає масив (array) екземплярів [MongoDBDriverServer](class.mongodb-driver-server.md), до яких підключено поточного менеджера.

> **Зауваження**: Оскільки драйвер підключається до бази даних ліниво, цей метод може повертати порожній масив (array), якщо він викликається перед виконанням операції в [MongoDBDriverManager](class.mongodb-driver-manager.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив (array) екземплярів [MongoDBDriverServer](class.mongodb-driver-server.md), до яких підключено менеджера.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverManager::getServers()****

```php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");

/* Из-за того, что драйвер подключается к серверу лениво, вызов Manager::getServers()
 * первоначально может вернуть пустой Масив. */
var_dump($manager->getServers());

$command = new MongoDB\Driver\Command(['ping' => 1]);
$manager->executeCommand('db', $command);

var_dump($manager->getServers());

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(0) {
}
array(1) {
  [0]=>
  object(MongoDB\Driver\Server)#3 (10) {
    ["host"]=>
    string(9) "localhost"
    ["port"]=>
    int(27017)
    ["type"]=>
    int(1)
    ["is_primary"]=>
    bool(false)
    ["is_secondary"]=>
    bool(false)
    ["is_arbiter"]=>
    bool(false)
    ["is_hidden"]=>
    bool(false)
    ["is_passive"]=>
    bool(false)
    ["last_hello_response"]=>
    array(8) {
      ["isWritablePrimary"]=>
      bool(true)
      ["maxBsonObjectSize"]=>
      int(16777216)
      ["maxMessageSizeBytes"]=>
      int(48000000)
      ["maxWriteBatchSize"]=>
      int(1000)
      ["localTime"]=>
      object(MongoDB\BSON\UTCDateTime)#4 (1) {
        ["milliseconds"]=>
        int(1447267964517)
      }
      ["maxWireVersion"]=>
      int(3)
      ["minWireVersion"]=>
      int(0)
      ["ok"]=>
      float(1)
    }
    ["round_trip_time"]=>
    int(554)
  }
}
```

### Дивіться також

-   [MongoDBDriverServer](class.mongodb-driver-server.md)
-   [MongoDBDriverManager::selectServer()](mongodb-driver-manager.selectserver.md) - Вибрати сервер, що відповідає перевагам читання
