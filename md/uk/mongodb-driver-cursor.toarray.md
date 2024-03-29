---
navigation:
  - mongodb-driver-cursor.settypemap.md: '« MongoDB\\Driver\\Cursor::setTypeMap'
  - mongodb-driver-cursor.valid.md: 'MongoDB\\Driver\\Cursor::valid »'
  - index.md: PHP Manual
  - class.mongodb-driver-cursor.md: MongoDB\\Driver\\Cursor
title: 'MongoDB\\Driver\\Cursor::toArray'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Cursor::toArray

(mongodb >=1.0.0)

MongoDB\\Driver\\Cursor::toArray — Повертає масив, що містить усі результати курсору

### Опис

```methodsynopsis
final public MongoDB\Driver\Cursor::toArray(): array
```

Ітерує курсор та повертає його результати у вигляді масиву . [MongoDB\\Driver\\Cursor::setTypeMap()](mongodb-driver-cursor.settypemap.md) може використовуватися для керування тим, як документи десеріалізовані до значення PHP.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив (array), що містить усі результати курсору.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання** MongoDB\\Driver\\Cursor::toArray()\*\*\*\*

```php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);
$bulk->insert(['x' => 2]);
$bulk->insert(['x' => 3]);
$manager->executeBulkWrite('db.collection', $bulk);

$query = new MongoDB\Driver\Query([]);
$cursor = $manager->executeQuery('db.collection', $query);

var_dump($cursor->toArray());

?>
```

Висновок наведеного прикладу буде схожим на:

```
array(3) {
  [0]=>
  object(stdClass)#6 (2) {
    ["_id"]=>
    object(MongoDB\BSON\ObjectId)#5 (1) {
      ["oid"]=>
      string(24) "564259a96118fd40b41bcf61"
    }
    ["x"]=>
    int(1)
  }
  [1]=>
  object(stdClass)#8 (2) {
    ["_id"]=>
    object(MongoDB\BSON\ObjectId)#7 (1) {
      ["oid"]=>
      string(24) "564259a96118fd40b41bcf62"
    }
    ["x"]=>
    int(2)
  }
  [2]=>
  object(stdClass)#10 (2) {
    ["_id"]=>
    object(MongoDB\BSON\ObjectId)#9 (1) {
      ["oid"]=>
      string(24) "564259a96118fd40b41bcf63"
    }
    ["x"]=>
    int(3)
  }
}
```

### Дивіться також

-   [MongoDB\\Driver\\Cursor::setTypeMap()](mongodb-driver-cursor.settypemap.md) \- Встановлює карту типу для десеріалізації BSON
