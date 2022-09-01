---
navigation:
  - mongodb-driver-writeresult.getmodifiedcount.html: '« MongoDBDriverWriteResult::getModifiedCount'
  - mongodb-driver-writeresult.getupsertedcount.html: 'MongoDBDriverWriteResult::getUpsertedCount »'
  - index.html: PHP Manual
  - class.mongodb-driver-writeresult.html: MongoDBDriverWriteResult
title: 'MongoDBDriverWriteResult::getServer'
---
# MongoDBDriverWriteResult::getServer

(mongodb >=1.0.0)

MongoDBDriverWriteResult::getServer — Повертає сервер, пов'язаний із цим результатом запису

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteResult::getServer(): MongoDB\Driver\Server
```

Повертає [MongoDBDriverServer](class.mongodb-driver-server.html), пов'язаний із цим результатом запису. Це сервер, який виконав [MongoDBDriverBulkWrite](class.mongodb-driver-bulkwrite.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDBDriverServer](class.mongodb-driver-server.md) пов'язаний із цим результатом запису.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

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

-   [MongoDBDriverServer](class.mongodb-driver-server.md)
