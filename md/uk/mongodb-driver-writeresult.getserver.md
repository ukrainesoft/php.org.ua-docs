Повертає сервер, пов'язаний із цим результатом запису

-   [« MongoDB\\Driver\\WriteResult::getModifiedCount](mongodb-driver-writeresult.getmodifiedcount.html)
    
-   [MongoDB\\Driver\\WriteResult::getUpsertedCount »](mongodb-driver-writeresult.getupsertedcount.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\WriteResult](class.mongodb-driver-writeresult.html)
    
-   Повертає сервер, пов'язаний із цим результатом запису
    

# MongoDBDriverWriteResult::getServer

(mongodb >=1.0.0)

MongoDBDriverWriteResult::getServer — Повертає сервер, пов'язаний із цим результатом запису

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteResult::getServer(): MongoDB\Driver\Server
```

Повертає [MongoDB\\Driver\\Server](class.mongodb-driver-server.html), пов'язаний із цим результатом запису. Це сервер, який виконав [MongoDB\\Driver\\BulkWrite](class.mongodb-driver-bulkwrite.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDB\\Driver\\Server](class.mongodb-driver-server.html) пов'язаний із цим результатом запису.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverWriteResult::getServer()****

```php
<?php

$manager = new MongoDB\Driver\Manager;
$server = $manager->selectServer(new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_PRIMARY));

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);

$result = $server->executeBulkWrite('db.collection', $bulk);

var_dump($result->getServer() == $server);

?>
```

Результат виконання цього прикладу:

```
bool(true)
```

### Дивіться також

-   [MongoDB\\Driver\\Server](class.mongodb-driver-server.html)