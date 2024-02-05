---
navigation:
  - mongodb-driver-bulkwrite.delete.md: '« MongoDB\\Driver\\BulkWrite::delete'
  - mongodb-driver-bulkwrite.update.md: 'MongoDB\\Driver\\BulkWrite::update »'
  - index.md: PHP Manual
  - class.mongodb-driver-bulkwrite.md: MongoDB\\Driver\\BulkWrite
title: 'MongoDB\\Driver\\BulkWrite::insert'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\BulkWrite::insert

(mongodb >=1.0.0)

MongoDB\\Driver\\BulkWrite::insert — Додати операцію вставки в порцію

### Опис

```methodsynopsis
public MongoDB\Driver\BulkWrite::insert(array|object $document): mixed
```

Добавляем операцию вставки в[MongoDB\\Driver\\BulkWrite](class.mongodb-driver-bulkwrite.md)

### Список параметрів

`document`(array|object)

Документ для вставлення.

### Значення, що повертаються

Повертає `_id`добавленного документа. Если в`document` не було задано `_id`, буде повернутий [MongoDB\\BSON\\ObjectId](class.mongodb-bson-objectid.md)згенерований для вставки.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.3.0 | Завжди повертається `_id` для доданого документа. Раніше метод повертав значення тільки якщо [MongoDB\\BSON\\ObjectId](class.mongodb-bson-objectid.md) був створений. |

### Приклади

**Пример #1 Пример использования**MongoDB\\Driver\\BulkWrite::insert()\*\*\*\*

```php
<?php

$bulk = new MongoDB\Driver\BulkWrite;

$document1 = ['title' => 'one'];
$document2 = ['_id' => 'custom ID', 'title' => 'two'];
$document3 = ['_id' => new MongoDB\BSON\ObjectId, 'title' => 'three'];

$_id1 = $bulk->insert($document1);
$_id2 = $bulk->insert($document2);
$_id3 = $bulk->insert($document3);

var_dump($_id1, $_id2, $_id3);

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
$result = $manager->executeBulkWrite('db.collection', $bulk);

?>
```

Висновок наведеного прикладу буде схожим на:

```
object(MongoDB\BSON\ObjectId)#3 (1) {
  ["oid"]=>
  string(24) "54d51146bd21b91405401d92"
}
NULL
NULL
```

### Дивіться також

-   [MongoDB\\Driver\\Manager::executeBulkWrite()](mongodb-driver-manager.executebulkwrite.md) \- Виконує одну або кілька операцій запису
-   [MongoDB\\Driver\\WriteResult](class.mongodb-driver-writeresult.md)
-   [MongoDB\\BSON\\ObjectId](class.mongodb-bson-objectid.md)
-   [MongoDB\\BSON\\Persistable](class.mongodb-bson-persistable.md)
