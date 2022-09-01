---
navigation:
  - mongodb-driver-writeresult.getdeletedcount.html: '« MongoDBDriverWriteResult::getDeletedCount'
  - mongodb-driver-writeresult.getmatchedcount.html: 'MongoDBDriverWriteResult::getMatchedCount »'
  - index.html: PHP Manual
  - class.mongodb-driver-writeresult.html: MongoDBDriverWriteResult
title: 'MongoDBDriverWriteResult::getInsertedCount'
---
# MongoDBDriverWriteResult::getInsertedCount

(mongodb >=1.0.0)

MongoDBDriverWriteResult::getInsertedCount — Повертає кількість вставлених документів (за винятком злиття)

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteResult::getInsertedCount(): ?int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає кількість вставлених документів (за винятком злиття) або **`null`** якщо запис не було підтверджено.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverWriteResult::getInsertedCount()****

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

var_dump($result->getInsertedCount());

?>
```

Результат виконання цього прикладу:

```
int(1)
```

### Дивіться також

-   [MongoDBDriverWriteResult::isAcknowledged()](mongodb-driver-writeresult.isacknowledged.html) - Повертає, чи був запис підтверджений
