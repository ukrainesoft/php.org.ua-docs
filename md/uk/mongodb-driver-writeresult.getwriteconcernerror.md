Повертає будь-яку помилку гарантій запису, що відбувся

-   [« MongoDBDriverWriteResult::getUpsertedIds](mongodb-driver-writeresult.getupsertedids.html)
    
-   [MongoDBDriverWriteResult::getWriteErrors »](mongodb-driver-writeresult.getwriteerrors.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverWriteResult](class.mongodb-driver-writeresult.html)
    
-   Повертає будь-яку помилку гарантій запису, що відбувся
    

# MongoDBDriverWriteResult::getWriteConcernError

(mongodb >=1.0.0)

MongoDBDriverWriteResult::getWriteConcernError — Повертає будь-яку помилку гарантій запису, яка сталася

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteResult::getWriteConcernError(): ?MongoDB\Driver\WriteConcernError
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDBDriverWriteConcernError](class.mongodb-driver-writeconcernerror.html), якщо під час операції запису сталася помилка гарантій запису, та **`null`** в іншому випадку.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverWriteResult::getWriteConcernError()****

```php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://rs1.example.com,rs2.example.com/?replicaSet=myReplicaSet");

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);

$writeConcern = new MongoDB\Driver\WriteConcern(2, 1);

try {
    $manager->executeBulkWrite('db.collection', $bulk, $writeConcern);
} catch(MongoDB\Driver\Exception\BulkWriteException $e) {
    var_dump($e->getWriteResult()->getWriteConcernError());
}

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(MongoDB\Driver\WriteConcernError)#6 (3) {
  ["message"]=>
  string(33) "waiting for replication timed out"
  ["code"]=>
  int(64)
  ["info"]=>
  object(stdClass)#7 (1) {
    ["wtimeout"]=>
    bool(true)
  }
}
```

### Дивіться також

-   [MongoDBDriverWriteConcern](class.mongodb-driver-writeconcern.html)
-   [» Справка по гарантиям записи](https://www.mongodb.com/docs/manual/reference/write-concern/)