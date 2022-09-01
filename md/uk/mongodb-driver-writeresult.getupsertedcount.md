---
navigation:
  - mongodb-driver-writeresult.getserver.html: '« MongoDBDriverWriteResult::getServer'
  - mongodb-driver-writeresult.getupsertedids.html: 'MongoDBDriverWriteResult::getUpsertedIds »'
  - index.html: PHP Manual
  - class.mongodb-driver-writeresult.html: MongoDBDriverWriteResult
title: 'MongoDBDriverWriteResult::getUpsertedCount'
---
# MongoDBDriverWriteResult::getUpsertedCount

(mongodb >=1.0.0)

MongoDBDriverWriteResult::getUpsertedCount — Повертає кількість документів, вставлених злиттям

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteResult::getUpsertedCount(): ?int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає кількість документів, які вставлені злиттям.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverWriteResult::getUpsertedCount()****

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

var_dump($result->getUpsertedCount());

?>
```

Результат виконання цього прикладу:

```
int(2)
```

### Дивіться також

-   [MongoDBDriverWriteResult::getUpsertedIds()](mongodb-driver-writeresult.getupsertedids.html) - Повертає масив ідентифікаторів для об'єднаних документів
-   [MongoDBDriverWriteResult::isAcknowledged()](mongodb-driver-writeresult.isacknowledged.html) - Повертає, чи був запис підтверджений
