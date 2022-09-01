---
navigation:
  - mongodb-driver-writeresult.getmatchedcount.html: '« MongoDBDriverWriteResult::getMatchedCount'
  - mongodb-driver-writeresult.getserver.html: 'MongoDBDriverWriteResult::getServer »'
  - index.md: PHP Manual
  - class.mongodb-driver-writeresult.html: MongoDBDriverWriteResult
title: 'MongoDBDriverWriteResult::getModifiedCount'
---
# MongoDBDriverWriteResult::getModifiedCount

(mongodb >=1.0.0)

MongoDBDriverWriteResult::getModifiedCount — Повертає кількість існуючих оновлених документів

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteResult::getModifiedCount(): ?int
```

Якщо операція оновлення не призводить до зміни документа (наприклад, встановлення значення поля в його поточне значення), змінене число може бути менше, ніж значення, що повертається [MongoDBDriverWriteResult::getMatchedCount()](mongodb-driver-writeresult.getmatchedcount.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає кількість існуючих оновлених документів або **`null`**, якщо запис не було підтверджено.

Змінений лічильник недоступний у версіях MongoDB до версії 2.6, де використовувалася застаріла версія проводового протоколу (тобто OPUPDATE). У цьому випадку змінена кількість також дорівнюватиме **`null`**

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverWriteResult::getModifiedCount()****

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

var_dump($result->getModifiedCount());

?>
```

Результат виконання цього прикладу:

```
int(1)
```

### Дивіться також

-   [MongoDBDriverWriteResult::getMatchedCount()](mongodb-driver-writeresult.getmatchedcount.html) - Повертає кількість документів, вибраних для оновлення
-   [MongoDBDriverWriteResult::isAcknowledged()](mongodb-driver-writeresult.isacknowledged.html) - Повертає, чи був запис підтверджений
