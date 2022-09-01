---
navigation:
  - class.mongodb-driver-exception-writeexception.html: « MongoDBDriverExceptionWriteException
  - mongodb.exceptions.tree.md: Class Tree »
  - index.md: PHP Manual
  - class.mongodb-driver-exception-writeexception.html: MongoDBDriverExceptionWriteException
title: 'MongoDBDriverExceptionWriteException::getWriteResult'
---
# MongoDBDriverExceptionWriteException::getWriteResult

(mongodb >= 1.0.0)

MongoDBDriverExceptionWriteException::getWriteResult — Повертає WriteResult для операції запису помилкою, що закінчилася.

### Опис

```methodsynopsis
final public MongoDB\Driver\Exception\WriteException::getWriteResult(): MongoDB\Driver\WriteResult
```

Повертає об'єкт [MongoDBDriverWriteResult](class.mongodb-driver-writeresult.html) для операції запису, що закінчилася помилкою. Більш детальну інформацію про помилку можна отримати за допомогою методів [MongoDBDriverWriteResult::getWriteErrors()](mongodb-driver-writeresult.getwriteerrors.html) і [MongoDBDriverWriteResult::getWriteConcernError()](mongodb-driver-writeresult.getwriteconcernerror.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт [MongoDBDriverWriteResult](class.mongodb-driver-writeresult.html) для операції запису помилкою, що закінчилася.

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverExceptionWriteException::getWriteResult()****

```php
<?php

$manager = new MongoDB\Driver\Manager('mongodb://localhost');
$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['_id' => 1]);
$bulk->insert(['_id' => 1]);

try {
    $manager->executeBulkWrite('db.collection', $bulk);
} catch (MongoDB\Driver\Exception\WriteException $e) {
    $writeResult = $e->getWriteResult();

    if ($writeConcernError = $writeResult->getWriteConcernError()) {
        var_dump($writeConcernError);
    }

    if ($writeErrors = $writeResult->getWriteErrors()) {
        var_dump($writeErrors);
    }
}

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(1) {
  [0]=>
  object(MongoDB\Driver\WriteError)#5 (4) {
    ["message"]=>
    string(70) "E11000 duplicate key error index: db.collection.$_id_ dup key: { : 1 }"
    ["code"]=>
    int(11000)
    ["index"]=>
    int(1)
    ["info"]=>
    NULL
  }
}
```

### Дивіться також

-   [MongoDBDriverWriteResult](class.mongodb-driver-writeresult.html)
-   [MongoDBDriverManager::executeBulkWrite()](mongodb-driver-manager.executebulkwrite.html) - Виконує одну або кілька операцій запису
