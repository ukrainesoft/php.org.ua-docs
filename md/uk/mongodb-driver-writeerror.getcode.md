Повертає код помилки WriteError

-   [« MongoDB\\Driver\\WriteError](class.mongodb-driver-writeerror.html)
    
-   [MongoDB\\Driver\\WriteError::getIndex »](mongodb-driver-writeerror.getindex.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\WriteError](class.mongodb-driver-writeerror.html)
    
-   Повертає код помилки WriteError
    

# MongoDBDriverWriteError::getCode

(mongodb >=1.0.0)

MongoDBDriverWriteError::getCode — Повертає код помилки WriteError

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteError::getCode(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає код помилки WriteError.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverWriteError::getCode()****

```php
<?php

$manager = new MongoDB\Driver\Manager;

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['_id' => 1]);
$bulk->insert(['_id' => 1]);

try {
    $manager->executeBulkWrite('db.collection', $bulk);
} catch(MongoDB\Driver\Exception\BulkWriteException $e) {
    var_dump($e->getWriteResult()->getWriteErrors()[0]->getCode());
}

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(11000)
```