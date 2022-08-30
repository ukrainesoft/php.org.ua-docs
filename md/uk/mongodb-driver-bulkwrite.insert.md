Додати операцію вставки в порцію

-   [« MongoDBDriverBulkWrite::delete](mongodb-driver-bulkwrite.delete.html)
    
-   [MongoDBDriverBulkWrite::update »](mongodb-driver-bulkwrite.update.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverBulkWrite](class.mongodb-driver-bulkwrite.html)
    
-   Додати операцію вставки в порцію
    

# MongoDBDriverBulkWrite::insert

(mongodb >=1.0.0)

MongoDBDriverBulkWrite::insert — Додати операцію вставки в порцію

### Опис

```methodsynopsis
public MongoDB\Driver\BulkWrite::insert(array|object $document): mixed
```

Додаємо операцію вставки в [MongoDBDriverBulkWrite](class.mongodb-driver-bulkwrite.html)

### Список параметрів

`document` (array | об'єкт)

Документ для вставлення.

### Значення, що повертаються

Повертає `_id` доданого документа. Якщо в `document` не було задано `_id`, буде повернутий [MongoDBBSONObjectId](class.mongodb-bson-objectid.html)згенерований для вставки.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### список змін

| Версия             | Описание                                                                                                                                                            |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PECL mongodb 1.3.0 | Завжди повертається `_id` для доданого документа. Раніше метод повертав значення тільки якщо [MongoDBBSONObjectId](class.mongodb-bson-objectid.html) був створений. |

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverBulkWrite::insert()****

```php
<?php

$bulk = new MongoDB\Driver\BulkWrite;

$document1 = ['title' => 'one'];
$document2 = ['_id' => 'custom ID', 'title' => 'two'];
$document3 = ['_id' => new MongoDB\BSON\ObjectId, 'title' => 'three'];

$_id1 = $bulk->insert($document1);
$_id2 = $bulk->insert($document2);
$_id3 = $bulk->insert($document3);

var_dump($_id1, $_id2, $_id3);

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
$result = $manager->executeBulkWrite('db.collection', $bulk);

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(MongoDB\BSON\ObjectId)#3 (1) {
  ["oid"]=>
  string(24) "54d51146bd21b91405401d92"
}
NULL
NULL
```

### Дивіться також

-   [MongoDBDriverManager::executeBulkWrite()](mongodb-driver-manager.executebulkwrite.html) - Виконує одну або кілька операцій запису
-   [MongoDBDriverWriteResult](class.mongodb-driver-writeresult.html)
-   [MongoDBBSONObjectId](class.mongodb-bson-objectid.html)
-   [MongoDBBSONPersistable](class.mongodb-bson-persistable.html)