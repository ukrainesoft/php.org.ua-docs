---
navigation:
  - mongodb-driver-writeconcernerror.getinfo.md: '« MongoDB\\Driver\\WriteConcernError::getInfo'
  - class.mongodb-driver-writeerror.md: MongoDB\\Driver\\WriteError »
  - index.md: PHP Manual
  - class.mongodb-driver-writeconcernerror.md: MongoDB\\Driver\\WriteConcernError
title: 'MongoDB\\Driver\\WriteConcernError::getMessage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\WriteConcernError::getMessage

(mongodb >=1.0.0)

MongoDB\\Driver\\WriteConcernError::getMessage — Повертає повідомлення про помилку WriteConcernError

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteConcernError::getMessage(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає повідомлення про помилку WriteConcernError.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання** MongoDB\\Driver\\WriteConcernError::getMessage()\*\*\*\*

```php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://rs1.example.com,rs2.example.com/?replicaSet=myReplicaSet");

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);

$writeConcern = new MongoDB\Driver\WriteConcern(2, 1);

try {
    $manager->executeBulkWrite('db.collection', $bulk, $writeConcern);
} catch(MongoDB\Driver\Exception\BulkWriteException $e) {
    var_dump($e->getWriteResult()->getWriteConcernError()->getMessage());
}

?>
```

Висновок наведеного прикладу буде схожим на:

```
string(33) "waiting for replication timed out"
```

### Дивіться також

-   [» Довідка по гарантіях запису](https://www.mongodb.com/docs/manual/reference/write-concern/)
