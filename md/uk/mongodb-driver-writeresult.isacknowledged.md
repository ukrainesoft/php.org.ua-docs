---
navigation:
  - mongodb-driver-writeresult.getwriteerrors.md: '« MongoDBDriverWriteResult::getWriteErrors'
  - book.bson.md: MongoDBBSON »
  - index.md: PHP Manual
  - class.mongodb-driver-writeresult.md: MongoDBDriverWriteResult
title: 'MongoDBDriverWriteResult::isAcknowledged'
---
# MongoDBDriverWriteResult::isAcknowledged

(mongodb >=1.0.0)

MongoDBDriverWriteResult::isAcknowledged — Повертає, чи був запис підтверджений

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteResult::isAcknowledged(): bool
```

Якщо запис підтверджено, інші поля будуть доступні в об'єкті [MongoDBDriverWriteResult](class.mongodb-driver-writeresult.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо запис було підтверджено, та **`false`** в іншому випадку.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverWriteResult::isAcknowledged()** з підтвердженими гарантіями запису**

```php
<?php

$manager = new MongoDB\Driver\Manager;

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);

$result = $manager->executeBulkWrite('db.collection', $bulk);

var_dump($result->isAcknowledged());

?>
```

Результат виконання цього прикладу:

```
bool(true)
```

**Приклад #2 Приклад використання **MongoDBDriverWriteResult::isAcknowledged()** з непідтвердженими гарантіями запису**

```php
<?php

$manager = new MongoDB\Driver\Manager;

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);

$result = $manager->executeBulkWrite('db.collection', $bulk, new MongoDB\Driver\WriteConcern(0));

var_dump($result->isAcknowledged());

?>
```

Результат виконання цього прикладу:

```
bool(false)
```

### Дивіться також

-   [MongoDBDriverWriteConcern](class.mongodb-driver-writeconcern.md)
-   [» Справка по гарантиям записи](https://www.mongodb.com/docs/manual/reference/write-concern/)
