- [« MongoDB\Driver\WriteResult::getModifiedCount](mongodb-driver-writeresult.getmodifiedcount.md)
- [MongoDB\Driver\WriteResult::getUpsertedCount »](mongodb-driver-writeresult.getupsertedcount.md)

- [PHP Manual](index.md)
- [MongoDB\Driver\WriteResult](class.mongodb-driver-writeresult.md)
- Повертає сервер, пов'язаний із цим результатом запису

# MongoDB\Driver\WriteResult::getServer

(mongodb \>=1.0.0)

MongoDB\Driver\WriteResult::getServer — Повертає сервер, пов'язаний з
цим результатом запису

### Опис

final public **MongoDB\Driver\WriteResult::getServer**():
[MongoDB\Driver\Server](class.mongodb-driver-server.md)

Повертає [MongoDB\Driver\Server](class.mongodb-driver-server.md),
пов'язаний із цим результатом запису. Це сервер, який виконав
[MongoDB\Driver\BulkWrite](class.mongodb-driver-bulkwrite.md).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDB\Driver\Server](class.mongodb-driver-server.md)
пов'язаний із цим результатом запису.

### Помилки

- При помилці парсингу аргумент кидає виняток
[MongoDB\Driver\Exception\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md).

### Приклади

**Приклад #1 Приклад використання
**MongoDB\Driver\WriteResult::getServer()****

` <?php$manager = new MongoDB\Driver\Manager;$server = $manager->selectServer(new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_PRIMARY));$bulk = new Mong ;$bulk->insert(['x' => 1]);$result = $server->executeBulkWrite('db.collection', $bulk);var_dump($result->getServer() == $server) ;?> `

Результат виконання цього прикладу:

bool(true)

### Дивіться також

- [MongoDB\Driver\Server](class.mongodb-driver-server.md)
