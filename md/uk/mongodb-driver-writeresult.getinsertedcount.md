---
navigation:
  - mongodb-driver-writeresult.getdeletedcount.md: '« MongoDB\\Driver\\WriteResult::getDeletedCount'
  - mongodb-driver-writeresult.getmatchedcount.md: 'MongoDB\\Driver\\WriteResult::getMatchedCount »'
  - index.md: PHP Manual
  - class.mongodb-driver-writeresult.md: MongoDB\\Driver\\WriteResult
title: 'MongoDB\\Driver\\WriteResult::getInsertedCount'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\WriteResult::getInsertedCount

(mongodb >=1.0.0)

MongoDB\\Driver\\WriteResult::getInsertedCount — Повертає кількість вставлених документів (за винятком злиття)

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteResult::getInsertedCount(): ?int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає кількість вставлених документів (за винятком злиття) або **`null`** якщо запис не було підтверджено.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання** MongoDB\\Driver\\WriteResult::getInsertedCount()\*\*\*\*

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

var_dump($result->getInsertedCount());

?>
```

Результат виконання наведеного прикладу:

```
int(1)
```

### Дивіться також

-   [MongoDB\\Driver\\WriteResult::isAcknowledged()](mongodb-driver-writeresult.isacknowledged.md) \- Повертає, чи був запис підтверджений
