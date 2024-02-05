---
navigation:
  - mongodb-driver-writeresult.getupsertedids.md: '« MongoDB\\Driver\\WriteResult::getUpsertedIds'
  - mongodb-driver-writeresult.getwriteerrors.md: 'MongoDB\\Driver\\WriteResult::getWriteErrors »'
  - index.md: PHP Manual
  - class.mongodb-driver-writeresult.md: MongoDB\\Driver\\WriteResult
title: 'MongoDB\\Driver\\WriteResult::getWriteConcernError'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\WriteResult::getWriteConcernError

(mongodb >=1.0.0)

MongoDB\\Driver\\WriteResult::getWriteConcernError — Повертає будь-яку помилку гарантій запису, яка сталася

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteResult::getWriteConcernError(): ?MongoDB\Driver\WriteConcernError
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDB\\Driver\\WriteConcernError](class.mongodb-driver-writeconcernerror.md), якщо під час операції запису сталася помилка гарантій запису, та **`null`** в іншому випадку.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Пример #1 Пример использования**MongoDB\\Driver\\WriteResult::getWriteConcernError()\*\*\*\*

```php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://rs1.example.com,rs2.example.com/?replicaSet=myReplicaSet");

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);

$writeConcern = new MongoDB\Driver\WriteConcern(2, 1);

try {
    $manager->executeBulkWrite('db.collection', $bulk, $writeConcern);
} catch(MongoDB\Driver\Exception\BulkWriteException $e) {
    var_dump($e->getWriteResult()->getWriteConcernError());
}

?>
```

Висновок наведеного прикладу буде схожим на:

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

-   [MongoDB\\Driver\\WriteConcern](class.mongodb-driver-writeconcern.md)
-   [» Довідка по гарантіях запису](https://www.mongodb.com/docs/manual/reference/write-concern/)
