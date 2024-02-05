---
navigation:
  - class.mongodb-driver-writeconcernerror.md: « MongoDB\\Driver\\WriteConcernError
  - mongodb-driver-writeconcernerror.getinfo.md: 'MongoDB\\Driver\\WriteConcernError::getInfo »'
  - index.md: PHP Manual
  - class.mongodb-driver-writeconcernerror.md: MongoDB\\Driver\\WriteConcernError
title: 'MongoDB\\Driver\\WriteConcernError::getCode'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\WriteConcernError::getCode

(mongodb >=1.0.0)

MongoDB\\Driver\\WriteConcernError::getCode — Повертає код помилки WriteConcernError

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteConcernError::getCode(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає код помилки WriteConcernError.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання** MongoDB\\Driver\\WriteConcernError::getCode()\*\*\*\*

```php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://rs1.example.com,rs2.example.com/?replicaSet=myReplicaSet");

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);

$writeConcern = new MongoDB\Driver\WriteConcern(2, 1);

try {
    $manager->executeBulkWrite('db.collection', $bulk, $writeConcern);
} catch(MongoDB\Driver\Exception\BulkWriteException $e) {
    var_dump($e->getWriteResult()->getWriteConcernError()->getCode());
}

?>
```

Висновок наведеного прикладу буде схожим на:

```
int(64)
```

### Дивіться також

-   [» Довідка по гарантіях запису](https://www.mongodb.com/docs/manual/reference/write-concern/)
