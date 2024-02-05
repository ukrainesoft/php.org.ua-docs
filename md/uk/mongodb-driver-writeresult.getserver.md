---
navigation:
  - mongodb-driver-writeresult.getmodifiedcount.md: '« MongoDB\\Driver\\WriteResult::getModifiedCount'
  - mongodb-driver-writeresult.getupsertedcount.md: 'MongoDB\\Driver\\WriteResult::getUpsertedCount »'
  - index.md: PHP Manual
  - class.mongodb-driver-writeresult.md: MongoDB\\Driver\\WriteResult
title: 'MongoDB\\Driver\\WriteResult::getServer'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\WriteResult::getServer

(mongodb >=1.0.0)

MongoDB\\Driver\\WriteResult::getServer — Повертає сервер, пов'язаний із цим результатом запису

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteResult::getServer(): MongoDB\Driver\Server
```

Повертає [MongoDB\\Driver\\Server](class.mongodb-driver-server.md), пов'язаний із цим результатом запису. Це сервер, який виконав [MongoDB\\Driver\\BulkWrite](class.mongodb-driver-bulkwrite.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDB\\Driver\\Server](class.mongodb-driver-server.md) пов'язаний із цим результатом запису.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання** MongoDB\\Driver\\WriteResult::getServer()\*\*\*\*

```php
<?php

$manager = new MongoDB\Driver\Manager;
$server = $manager->selectServer(new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_PRIMARY));

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);

$result = $server->executeBulkWrite('db.collection', $bulk);

var_dump($result->getServer() == $server);

?>
```

Результат виконання наведеного прикладу:

```
bool(true)
```

### Дивіться також

-   [MongoDB\\Driver\\Server](class.mongodb-driver-server.md)
