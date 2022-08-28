Встановлює карту типу для десеріалізації BSON

-   [« MongoDB\\Driver\\Cursor::rewind](mongodb-driver-cursor.rewind.html)
    
-   [MongoDB\\Driver\\Cursor::toArray »](mongodb-driver-cursor.toarray.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Cursor](class.mongodb-driver-cursor.html)
    
-   Встановлює карту типу для десеріалізації BSON
    

# MongoDBDriverCursor::setTypeMap

(mongodb >=1.0.0)

MongoDBDriverCursor::setTypeMap — Встановлює карту типу для десеріалізації BSON

### Опис

```methodsynopsis
final public MongoDB\Driver\Cursor::setTypeMap(array $typemap): void
```

Встановлює [конфигурацию карты типов](mongodb.persistence.deserialization.html#mongodb.persistence.typemaps), яка буде використовуватися при десеріалізації результатів BSON значення PHP.

### Список параметрів

`typeMap` (array)

[Конфигурация карты типов](mongodb.persistence.deserialization.html#mongodb.persistence.typemaps)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

При ітерації курсором може викидатися такі винятки через неправильну конфігурацію карти типів:

-   Викидає [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)якщо клас на карті типів не може бути створений або не реалізує [MongoDB\\BSON\\Unserializable](class.mongodb-bson-unserializable.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverCursor::setTypeMap()****

```php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");

$bulk = new MongoDB\Driver\BulkWrite;
$id = $bulk->insert(['x' => 1]);
$manager->executeBulkWrite('db.collection', $bulk);

$query = new MongoDB\Driver\Query(['_id' => $id]);
$cursor = $manager->executeQuery('db.collection', $query);
$cursor->setTypeMap(['root' => 'array']);

foreach ($cursor as $document) {
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

-   [Постоянные данные](mongodb.persistence.html)