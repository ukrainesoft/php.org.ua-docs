---
navigation:
  - mongodb-driver-writeconcernerror.getcode.md: '« MongoDB\\Driver\\WriteConcernError::getCode'
  - mongodb-driver-writeconcernerror.getmessage.md: 'MongoDB\\Driver\\WriteConcernError::getMessage »'
  - index.md: PHP Manual
  - class.mongodb-driver-writeconcernerror.md: MongoDB\\Driver\\WriteConcernError
title: 'MongoDB\\Driver\\WriteConcernError::getInfo'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\WriteConcernError::getInfo

(mongodb >=1.0.0)

MongoDB\\Driver\\WriteConcernError::getInfo — Повертає документ метаданих для WriteConcernError

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteConcernError::getInfo(): ?object
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає документ метаданих для WriteConcernError або \*\*`null`\*\*якщо немає метаданих.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання** MongoDB\\Driver\\WriteConcernError::getInfo()\*\*\*\*

```php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://rs1.example.com,rs2.example.com/?replicaSet=myReplicaSet");

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);

$writeConcern = new MongoDB\Driver\WriteConcern(2, 1);

try {
    $manager->executeBulkWrite('db.collection', $bulk, $writeConcern);
} catch(MongoDB\Driver\Exception\BulkWriteException $e) {
    var_dump($e->getWriteResult()->getWriteConcernError()->getInfo());
}

?>
```

Висновок наведеного прикладу буде схожим на:

```
object(stdClass)#1 (1) {
  ["wtimeout"]=>
  bool(true)
}
```

### Дивіться також

-   [» Довідка по гарантіях запису](https://www.mongodb.com/docs/manual/reference/write-concern/)
