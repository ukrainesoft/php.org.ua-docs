---
navigation:
  - mongodb-driver-writeresult.getmatchedcount.md: '« MongoDB\\Driver\\WriteResult::getMatchedCount'
  - mongodb-driver-writeresult.getserver.md: 'MongoDB\\Driver\\WriteResult::getServer »'
  - index.md: PHP Manual
  - class.mongodb-driver-writeresult.md: MongoDB\\Driver\\WriteResult
title: 'MongoDB\\Driver\\WriteResult::getModifiedCount'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\WriteResult::getModifiedCount

(mongodb >=1.0.0)

MongoDB\\Driver\\WriteResult::getModifiedCount — Повертає кількість існуючих оновлених документів

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteResult::getModifiedCount(): ?int
```

Якщо операція оновлення не призводить до зміни документа (наприклад, встановлення значення поля в його поточне значення), змінене число може бути менше, ніж значення, що повертається [MongoDB\\Driver\\WriteResult::getMatchedCount()](mongodb-driver-writeresult.getmatchedcount.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає кількість існуючих оновлених документів або **`null`**, якщо запис не було підтверджено.

Змінений лічильник недоступний у версіях MongoDB до версії 2.6, де використовувалася застаріла версія проводового протоколу (тобто OP\_UPDATE). У цьому випадку змінена кількість також дорівнюватиме **`null`**

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання** MongoDB\\Driver\\WriteResult::getModifiedCount()\*\*\*\*

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

var_dump($result->getModifiedCount());

?>
```

Результат виконання наведеного прикладу:

```
int(1)
```

### Дивіться також

-   [MongoDB\\Driver\\WriteResult::getMatchedCount()](mongodb-driver-writeresult.getmatchedcount.md) \- Повертає кількість документів, вибраних для оновлення
-   [MongoDB\\Driver\\WriteResult::isAcknowledged()](mongodb-driver-writeresult.isacknowledged.md) \- Повертає, чи був запис підтверджений
