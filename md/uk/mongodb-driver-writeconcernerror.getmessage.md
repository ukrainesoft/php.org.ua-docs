---
navigation:
  - mongodb-driver-writeconcernerror.getinfo.md: '« MongoDBDriverWriteConcernError::getInfo'
  - class.mongodb-driver-writeerror.md: MongoDBDriverWriteError »
  - index.md: PHP Manual
  - class.mongodb-driver-writeconcernerror.md: MongoDBDriverWriteConcernError
title: 'MongoDBDriverWriteConcernError::getMessage'
---
# MongoDBDriverWriteConcernError::getMessage

(mongodb >=1.0.0)

MongoDBDriverWriteConcernError::getMessage — Повертає повідомлення про помилку WriteConcernError

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteConcernError::getMessage(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає повідомлення про помилку WriteConcernError.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverWriteConcernError::getMessage()****

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

Результатом виконання цього прикладу буде щось подібне:

```
string(33) "waiting for replication timed out"
```

### Дивіться також

-   [» Справка по гарантиям записи](https://www.mongodb.com/docs/manual/reference/write-concern/)
