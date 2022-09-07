---
navigation:
  - mongodb-driver-cursor.rewind.md: '« MongoDBDriverCursor::rewind'
  - mongodb-driver-cursor.toarray.md: 'MongoDBDriverCursor::toArray »'
  - index.md: PHP Manual
  - class.mongodb-driver-cursor.md: MongoDBDriverCursor
title: 'MongoDBDriverCursor::setTypeMap'
---
# MongoDBDriverCursor::setTypeMap

(mongodb >=1.0.0)

MongoDBDriverCursor::setTypeMap — Встановлює карту типу для десеріалізації BSON

### Опис

```methodsynopsis
final public MongoDB\Driver\Cursor::setTypeMap(array $typemap): void
```

Встановлює [конфігурацію карти типів](mongodb.persistence.deserialization.md#mongodb.persistence.typemaps), яка буде використовуватися при десеріалізації результатів BSON значення PHP.

### Список параметрів

`typeMap` (array)

[Конфігурація карти типів](mongodb.persistence.deserialization.md#mongodb.persistence.typemaps)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

При ітерації курсором може викидатися такі винятки через неправильну конфігурацію карти типів:

-   Викидає [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо клас на карті типів не може бути створений або не реалізує [MongoDBBSONUnserializable](class.mongodb-bson-unserializable.md)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverCursor::setTypeMap()****

```php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");

$bulk = new MongoDB\Driver\BulkWrite;
$id = $bulk->insert(['x' => 1]);
$manager->executeBulkWrite('db.collection', $bulk);

$query = new MongoDB\Driver\Query(['_id' => $id]);
$cursor = $manager->executeQuery('db.collection', $query);
$cursor->setTypeMap(['root' => 'array']);

foreach ($cursor as $document) {
    var_dump($document);
}

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(2) {
  ["_id"]=>
  object(MongoDB\BSON\ObjectId)#6 (1) {
    ["oid"]=>
    string(24) "56424fb76118fd3267180741"
  }
  ["x"]=>
  int(1)
}
```

### Дивіться також

-   [Постійні дані](mongodb.persistence.md)
