Рядкове подання ідентифікатора курсора

-   [« MongoDBDriverCursorId::serialize](mongodb-driver-cursorid.serialize.html)
    
-   [MongoDBDriverCursorId::unserialize »](mongodb-driver-cursorid.unserialize.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverCursorId](class.mongodb-driver-cursorid.html)
    
-   Рядкове подання ідентифікатора курсора
    

# MongoDBDriverCursorId::function toString() { \[native code\] }

(mongodb >=1.0.0)

MongoDBDriverCursorId::toString — Строкове представлення ідентифікатора курсору

### Опис

```methodsynopsis
final public MongoDB\Driver\CursorId::__toString(): string
```

Повертає ідентифікатор курсору у вигляді рядка (string).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор курсору у вигляді рядка (string).

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverCursorId::toString()****

```php
<?php

/* В этом примере мы добавляем документы в коллекцию и указываем
 * меньший batchSize, чтобы гарантировать, что первая порция содержит только подмножество
 * наших результатов и курсор остаётся открытым на сервере. */
$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");
$query = new MongoDB\Driver\Query([], ['batchSize' => 2]);

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);
$bulk->insert(['x' => 2]);
$bulk->insert(['x' => 3]);
$manager->executeBulkWrite('db.collection', $bulk);

$cursor = $manager->executeQuery('db.collection', $query);
var_dump((string) $cursor->getId());

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(11) "98061641158"
```

### Дивіться також

-   [MongoDBDriverCursor::getId()](mongodb-driver-cursor.getid.html) - Повертає ідентифікатор для курсору