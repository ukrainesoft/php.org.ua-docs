---
navigation:
  - mongodb-driver-writeresult.getserver.md: '« MongoDB\\Driver\\WriteResult::getServer'
  - mongodb-driver-writeresult.getupsertedids.md: 'MongoDB\\Driver\\WriteResult::getUpsertedIds »'
  - index.md: PHP Manual
  - class.mongodb-driver-writeresult.md: MongoDB\\Driver\\WriteResult
title: 'MongoDB\\Driver\\WriteResult::getUpsertedCount'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\WriteResult::getUpsertedCount

(mongodb >=1.0.0)

MongoDB\\Driver\\WriteResult::getUpsertedCount — Повертає кількість документів, вставлених злиттям

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteResult::getUpsertedCount(): ?int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає кількість документів, які вставлені злиттям.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Пример #1 Пример использования**MongoDB\\Driver\\WriteResult::getUpsertedCount()\*\*\*\*

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

var_dump($result->getUpsertedCount());

?>
```

Результат виконання наведеного прикладу:

```
int(2)
```

### Дивіться також

-   [MongoDB\\Driver\\WriteResult::getUpsertedIds()](mongodb-driver-writeresult.getupsertedids.md) \- Повертає масив ідентифікаторів для об'єднаних документів
-   [MongoDB\\Driver\\WriteResult::isAcknowledged()](mongodb-driver-writeresult.isacknowledged.md) \- Повертає, чи був запис підтверджений
