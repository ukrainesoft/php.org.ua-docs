---
navigation:
  - class.mongodb-driver-writeresult.md: « MongoDB\\Driver\\WriteResult
  - mongodb-driver-writeresult.getinsertedcount.md: 'MongoDB\\Driver\\WriteResult::getInsertedCount »'
  - index.md: PHP Manual
  - class.mongodb-driver-writeresult.md: MongoDB\\Driver\\WriteResult
title: 'MongoDB\\Driver\\WriteResult::getDeletedCount'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\WriteResult::getDeletedCount

(mongodb >=1.0.0)

MongoDB\\Driver\\WriteResult::getDeletedCount — Повертає кількість видалених документів

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteResult::getDeletedCount(): ?int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає кількість видалених документів або **`null`** якщо запис не було підтверджено.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Пример #1 Пример использования**MongoDB\\Driver\\WriteResult::getDeletedCount()\*\*\*\*

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

var_dump($result->getDeletedCount());

?>
```

Результат виконання наведеного прикладу:

```
int(1)
```

### Дивіться також

-   [MongoDB\\Driver\\WriteResult::isAcknowledged()](mongodb-driver-writeresult.isacknowledged.md) \- Повертає, чи був запис підтверджений
