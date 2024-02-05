---
navigation:
  - mongodb-driver-writeresult.getwriteerrors.md: '« MongoDB\\Driver\\WriteResult::getWriteErrors'
  - book.bson.md: MongoDB\\BSON »
  - index.md: PHP Manual
  - class.mongodb-driver-writeresult.md: MongoDB\\Driver\\WriteResult
title: 'MongoDB\\Driver\\WriteResult::isAcknowledged'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\WriteResult::isAcknowledged

(mongodb >=1.0.0)

MongoDB\\Driver\\WriteResult::isAcknowledged — Повертає, чи був запис підтверджений

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteResult::isAcknowledged(): bool
```

Якщо запис підтверджено, інші поля будуть доступні в об'єкті [MongoDB\\Driver\\WriteResult](class.mongodb-driver-writeresult.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо запис було підтверджено, та **`false`** в іншому випадку.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Пример #1 Пример использования**MongoDB\\Driver\\WriteResult::isAcknowledged()\*\* з підтвердженими гарантіями запису\*\*

```php
<?php

$manager = new MongoDB\Driver\Manager;

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);

$result = $manager->executeBulkWrite('db.collection', $bulk);

var_dump($result->isAcknowledged());

?>
```

Результат виконання наведеного прикладу:

```
bool(true)
```

**Пример #2 Пример использования**MongoDB\\Driver\\WriteResult::isAcknowledged()\*\* з непідтвердженими гарантіями запису\*\*

```php
<?php

$manager = new MongoDB\Driver\Manager;

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);

$result = $manager->executeBulkWrite('db.collection', $bulk, new MongoDB\Driver\WriteConcern(0));

var_dump($result->isAcknowledged());

?>
```

Результат виконання наведеного прикладу:

```
bool(false)
```

### Дивіться також

-   [MongoDB\\Driver\\WriteConcern](class.mongodb-driver-writeconcern.md)
-   [» Довідка по гарантіях запису](https://www.mongodb.com/docs/manual/reference/write-concern/)
