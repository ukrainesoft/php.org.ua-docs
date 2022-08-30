Повертає кількість видалених документів

-   [« MongoDBDriverWriteResult](class.mongodb-driver-writeresult.html)
    
-   [MongoDBDriverWriteResult::getInsertedCount »](mongodb-driver-writeresult.getinsertedcount.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverWriteResult](class.mongodb-driver-writeresult.html)
    
-   Повертає кількість видалених документів
    

# MongoDBDriverWriteResult::getDeletedCount

(mongodb >=1.0.0)

MongoDBDriverWriteResult::getDeletedCount — Повертає кількість видалених документів

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteResult::getDeletedCount(): ?int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає кількість видалених документів або **`null`** якщо запис не було підтверджено.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverWriteResult::getDeletedCount()****

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

var_dump($result->getDeletedCount());

?>
```

Результат виконання цього прикладу:

```
int(1)
```

### Дивіться також

-   [MongoDBDriverWriteResult::isAcknowledged()](mongodb-driver-writeresult.isacknowledged.html) - Повертає, чи був запис підтверджений