---
navigation:
  - mongodb-driver-writeconcernerror.getcode.md: '« MongoDBDriverWriteConcernError::getCode'
  - mongodb-driver-writeconcernerror.getmessage.md: 'MongoDBDriverWriteConcernError::getMessage »'
  - index.md: PHP Manual
  - class.mongodb-driver-writeconcernerror.md: MongoDBDriverWriteConcernError
title: 'MongoDBDriverWriteConcernError::getInfo'
---
# MongoDBDriverWriteConcernError::getInfo

(mongodb >=1.0.0)

MongoDBDriverWriteConcernError::getInfo — Повертає документ метаданих для WriteConcernError

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteConcernError::getInfo(): ?object
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає документ метаданих для WriteConcernError або \*\*`null`\*\*якщо немає метаданих.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverWriteConcernError::getInfo()****

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

Результатом виконання цього прикладу буде щось подібне:

```
object(stdClass)#1 (1) {
  ["wtimeout"]=>
  bool(true)
}
```

### Дивіться також

-   [» Справка по гарантиям записи](https://www.mongodb.com/docs/manual/reference/write-concern/)
