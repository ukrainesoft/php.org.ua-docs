---
navigation:
  - mongodb-driver-writeresult.getupsertedcount.md: '« MongoDBDriverWriteResult::getUpsertedCount'
  - mongodb-driver-writeresult.getwriteconcernerror.md: 'MongoDBDriverWriteResult::getWriteConcernError »'
  - index.md: PHP Manual
  - class.mongodb-driver-writeresult.md: MongoDBDriverWriteResult
title: 'MongoDBDriverWriteResult::getUpsertedIds'
---
# MongoDBDriverWriteResult::getUpsertedIds

(mongodb >=1.0.0)

MongoDBDriverWriteResult::getUpsertedIds — Повертає масив ідентифікаторів для об'єднаних документів

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteResult::getUpsertedIds(): array
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив ідентифікаторів (тобто значення полів `"_id"`) для об'єднаних документів. Ключі масиву будуть відповідати індексу операції запису (з [MongoDBDriverBulkWrite](class.mongodb-driver-bulkwrite.md)), відповідальної за злиття.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverWriteResult::getUpsertedIds()****

```php
<?php

$manager = new MongoDB\Driver\Manager;

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);
$bulk->update(['x' => 1], ['$set' => ['y' => 3]]);
$bulk->update(['x' => 2], ['$set' => ['y' => 1]], ['upsert' => true]);
$bulk->update(['x' => 3], ['$set' => ['y' => 2]], ['upsert' => true]);
$bulk->delete(['x' => 1]);

$result = $manager->executeBulkWrite('db.collection', $bulk);

var_dump($result->getUpsertedIds());

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(2) {
  [2]=>
  object(MongoDB\BSON\ObjectId)#4 (1) {
    ["oid"]=>
    string(24) "580e62a224f2302f191b880b"
  }
  [3]=>
  object(MongoDB\BSON\ObjectId)#5 (1) {
    ["oid"]=>
    string(24) "580e62a224f2302f191b880c"
  }
}
```

### Дивіться також

-   [MongoDBDriverWriteResult::getUpsertedCount()](mongodb-driver-writeresult.getupsertedcount.md) - Повертає кількість документів, вставлених злиттям
-   [MongoDBDriverWriteResult::isAcknowledged()](mongodb-driver-writeresult.isacknowledged.md) - Повертає, чи був запис підтверджений
