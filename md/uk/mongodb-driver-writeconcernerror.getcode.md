---
navigation:
  - class.mongodb-driver-writeconcernerror.html: « MongoDBDriverWriteConcernError
  - mongodb-driver-writeconcernerror.getinfo.html: 'MongoDBDriverWriteConcernError::getInfo »'
  - index.md: PHP Manual
  - class.mongodb-driver-writeconcernerror.html: MongoDBDriverWriteConcernError
title: 'MongoDBDriverWriteConcernError::getCode'
---
# MongoDBDriverWriteConcernError::getCode

(mongodb >=1.0.0)

MongoDBDriverWriteConcernError::getCode — Повертає код помилки WriteConcernError

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteConcernError::getCode(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає код помилки WriteConcernError.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverWriteConcernError::getCode()****

```php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://rs1.example.com,rs2.example.com/?replicaSet=myReplicaSet");

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);

$writeConcern = new MongoDB\Driver\WriteConcern(2, 1);

try {
    $manager->executeBulkWrite('db.collection', $bulk, $writeConcern);
} catch(MongoDB\Driver\Exception\BulkWriteException $e) {
    var_dump($e->getWriteResult()->getWriteConcernError()->getCode());
}

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(64)
```

### Дивіться також

-   [» Справка по гарантиям записи](https://www.mongodb.com/docs/manual/reference/write-concern/)
