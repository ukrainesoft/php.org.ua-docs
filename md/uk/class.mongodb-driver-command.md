---
navigation:
  - mongodb-driver-manager.startsession.md: '« MongoDB\\Driver\\Manager::startSession'
  - mongodb-driver-command.construct.md: 'MongoDB\\Driver\\Command::\_\_construct »'
  - index.md: PHP Manual
  - book.mongodb.md: MongoDB\\Driver
title: Клас The MongoDB\\Driver\\Command
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас The MongoDB\\Driver\\Command

(mongodb >=1.0.0)

## Вступ

Класс**MongoDB\\Driver\\Command** - Це об'єкт значення, що представляє команду бази даних.

Щоб надати Помічників команд (Command Helpers) має бути створено об'єкт **MongoDB\\Driver\\Command**

## Огляд класів

```classsynopsis



    
     final
     
      class MongoDB\Driver\Command
     
     {


    /* Методы */
    
   final public __construct(array|object $document, ?array $commandOptions = null)

   }
```

## Приклади

**Приклад #1 Использование**MongoDB\\Driver\\Command**для предоставления помощника по созданию коллекций**

```php
<?php
class CreateCollection {
    protected $cmd = array();

    function __construct($collectionName) {
        $this->cmd["create"] = (string)$collectionName;
    }
    function setCappedCollection($maxBytes, $maxDocuments = false) {
        $this->cmd["capped"] = true;
        $this->cmd["size"]   = (int)$maxBytes;

        if ($maxDocuments) {
            $this->cmd["max"] = (int)$maxDocuments;
        }
    }
    function usePowerOf2Sizes($bool) {
        if ($bool) {
            $this->cmd["flags"] = 1;
        } else {
            $this->cmd["flags"] = 0;
        }
    }
    function setFlags($flags) {
        $this->cmd["flags"] = (int)$flags;
    }
    function getCommand() {
        return new MongoDB\Driver\Command($this->cmd);
    }
    function getCollectionName() {
        return $this->cmd["create"];
    }
}


$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");

$createCollection = new CreateCollection("cappedCollection");
$createCollection->setCappedCollection(64 * 1024);

try {
    $command = $createCollection->getCommand();
    $cursor = $manager->executeCommand("databaseName", $command);
    $response = $cursor->toArray()[0];
    var_dump($response);

    $collstats = ["collstats" => $createCollection->getCollectionName()];
    $cursor = $manager->executeCommand("databaseName", new MongoDB\Driver\Command($collstats));
    $response = $cursor->toArray()[0];
    var_dump($response);
} catch(MongoDB\Driver\Exception $e) {
    echo $e->getMessage(), "\n";
    exit;
}

?>
```

Результат виконання наведеного прикладу:

```
object(MongoDB\Driver\Command)#3 (1) {
  ["command"]=>
  array(3) {
    ["create"]=>
    string(16) "cappedCollection"
    ["capped"]=>
    bool(true)
    ["size"]=>
    int(65536)
  }
}
array(1) {
  ["ok"]=>
  float(1)
}
array(16) {
  ["ns"]=>
  string(29) "databaseName.cappedCollection"
  ["count"]=>
  int(0)
  ["size"]=>
  int(0)
  ["numExtents"]=>
  int(1)
  ["storageSize"]=>
  int(65536)
  ["nindexes"]=>
  int(1)
  ["lastExtentSize"]=>
  float(65536)
  ["paddingFactor"]=>
  float(1)
  ["paddingFactorNote"]=>
  string(101) "paddingFactor is unused and unmaintained in 2.8. It remains hard coded to 1.0 for compatibility only."
  ["userFlags"]=>
  int(0)
  ["capped"]=>
  bool(true)
  ["max"]=>
  int(9223372036854775807)
  ["maxSize"]=>
  int(65536)
  ["totalIndexSize"]=>
  int(8176)
  ["indexSizes"]=>
  object(stdClass)#4 (1) {
    ["_id_"]=>
    int(8176)
  }
  ["ok"]=>
  float(1)
}
```

## Зміст

-   [MongoDB\\Driver\\Command::\_\_construct](mongodb-driver-command.construct.md)— Створює новий об'єкт Command
