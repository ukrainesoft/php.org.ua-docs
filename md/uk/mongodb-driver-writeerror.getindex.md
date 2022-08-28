Повертає індекс запису, що відповідає цьому WriteError

-   [« MongoDB\\Driver\\WriteError::getCode](mongodb-driver-writeerror.getcode.html)
    
-   [MongoDB\\Driver\\WriteError::getInfo »](mongodb-driver-writeerror.getinfo.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\WriteError](class.mongodb-driver-writeerror.html)
    
-   Повертає індекс запису, що відповідає цьому WriteError
    

# MongoDBDriverWriteError::getIndex

(mongodb >=1.0.0)

MongoDBDriverWriteError::getIndex — Повертає індекс запису, який відповідає цьому WriteError

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteError::getIndex(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає індекс запису (з [MongoDB\\Driver\\BulkWrite](class.mongodb-driver-bulkwrite.html)), що відповідає поточному WriteError.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverWriteError::getIndex()****

```php
<?php

$manager = new MongoDB\Driver\Manager;

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['_id' => 1]);
$bulk->insert(['_id' => 1]);

try {
    $manager->executeBulkWrite('db.collection', $bulk);
} catch(MongoDB\Driver\Exception\BulkWriteException $e) {
    var_dump($e->getWriteResult()->getWriteErrors()[0]->getIndex());
}

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(1)
```

### Дивіться також

-   [MongoDB\\Driver\\BulkWrite](class.mongodb-driver-bulkwrite.html)