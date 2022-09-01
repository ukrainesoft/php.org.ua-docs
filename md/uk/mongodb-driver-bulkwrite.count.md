---
navigation:
  - mongodb-driver-bulkwrite.construct.html: '« MongoDBDriverBulkWrite::construct'
  - mongodb-driver-bulkwrite.delete.html: 'MongoDBDriverBulkWrite::delete »'
  - index.md: PHP Manual
  - class.mongodb-driver-bulkwrite.html: MongoDBDriverBulkWrite
title: 'MongoDBDriverBulkWrite::count'
---
# MongoDBDriverBulkWrite::count

(mongodb >=1.0.0)

MongoDBDriverBulkWrite::count — Підраховує кількість операцій запису в порції

### Опис

```methodsynopsis
public MongoDB\Driver\BulkWrite::count(): int
```

Повертає кількість операцій запису, доданих до об'єкту [MongoDBDriverBulkWrite](class.mongodb-driver-bulkwrite.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає кількість операцій запису, доданих до об'єкту [MongoDBDriverBulkWrite](class.mongodb-driver-bulkwrite.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.2.0 | Повертає кількість операцій запису, доданих до об'єкту [MongoDBDriverBulkWrite](class.mongodb-driver-bulkwrite.html). У попередніх версіях поверталося передбачувану кількість звернень клієнта до сервера, необхідні виконання всіх операцій записи. |

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverBulkWrite::count()****

```php
<?php

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['_id' => 1, 'x' => 1]);
$bulk->insert(['_id' => 2, 'x' => 2]);
$bulk->update(['x' => 2], ['$set' => ['x' => 1]]);
$bulk->delete(['x' => 1]);

var_dump(count($bulk));

?>
```

Результат виконання цього прикладу:

```
int(4)
```
