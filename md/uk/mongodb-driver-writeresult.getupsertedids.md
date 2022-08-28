Повертає масив ідентифікаторів для об'єднаних документів

-   [« MongoDB\\Driver\\WriteResult::getUpsertedCount](mongodb-driver-writeresult.getupsertedcount.html)
    
-   [MongoDB\\Driver\\WriteResult::getWriteConcernError »](mongodb-driver-writeresult.getwriteconcernerror.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\WriteResult](class.mongodb-driver-writeresult.html)
    
-   Повертає масив ідентифікаторів для об'єднаних документів
    

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

Повертає масив ідентифікаторів (тобто значення полів `"_id"`) для об'єднаних документів. Ключі масиву будуть відповідати індексу операції запису (з [MongoDB\\Driver\\BulkWrite](class.mongodb-driver-bulkwrite.html)), відповідальної за злиття.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverWriteResult::getUpsertedIds()****

```php
<?php

$manager = new MongoDB\Driver\Manager;

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);
$bulk->update(['x' => 1], ['$set' => ['y' => 3]]);
$bulk->update(['x' => 2], ['$set' => ['y' => 1]], ['upsert' => true]);
$bulk->update(['x' => 3], ['$set' => ['y' => 2]], ['upsert' => true]);
$bulk->delete(['x' => 1]);

$result = $manager->executeBulkWrite('db.collection', $bulk);

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

-   [MongoDB\\Driver\\WriteResult::getUpsertedCount()](mongodb-driver-writeresult.getupsertedcount.html) - Повертає кількість документів, вставлених злиттям
-   [MongoDB\\Driver\\WriteResult::isAcknowledged()](mongodb-driver-writeresult.isacknowledged.html) - Повертає, чи був запис підтверджений