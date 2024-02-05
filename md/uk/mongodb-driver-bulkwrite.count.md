---
navigation:
  - mongodb-driver-bulkwrite.construct.md: '« MongoDB\\Driver\\BulkWrite::\_\_construct'
  - mongodb-driver-bulkwrite.delete.md: 'MongoDB\\Driver\\BulkWrite::delete »'
  - index.md: PHP Manual
  - class.mongodb-driver-bulkwrite.md: MongoDB\\Driver\\BulkWrite
title: 'MongoDB\\Driver\\BulkWrite::count'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\BulkWrite::count

(mongodb >=1.0.0)

MongoDB\\Driver\\BulkWrite::count — Підраховує кількість операцій запису в порції

### Опис

```methodsynopsis
public MongoDB\Driver\BulkWrite::count(): int
```

Повертає кількість операцій запису, доданих до об'єкту [MongoDB\\Driver\\BulkWrite](class.mongodb-driver-bulkwrite.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає кількість операцій запису, доданих до об'єкту [MongoDB\\Driver\\BulkWrite](class.mongodb-driver-bulkwrite.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.2.0 | Повертає кількість операцій запису, доданих до об'єкту [MongoDB\\Driver\\BulkWrite](class.mongodb-driver-bulkwrite.md). . У попередніх версіях поверталося передбачувану кількість звернень клієнта до сервера, необхідні виконання всіх операцій записи. |

### Приклади

**Пример #1 Пример использования**MongoDB\\Driver\\BulkWrite::count()\*\*\*\*

```php
<?php

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['_id' => 1, 'x' => 1]);
$bulk->insert(['_id' => 2, 'x' => 2]);
$bulk->update(['x' => 2], ['$set' => ['x' => 1]]);
$bulk->delete(['x' => 1]);

var_dump(count($bulk));

?>
```

Результат виконання наведеного прикладу:

```
int(4)
```
