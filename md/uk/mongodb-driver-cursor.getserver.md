- [«MongoDB\Driver\Cursor::getId](mongodb-driver-cursor.getid.md)
- [MongoDB\Driver\Cursor::isDead »](mongodb-driver-cursor.isdead.md)

- [PHP Manual](index.md)
- [MongoDB\Driver\Cursor](class.mongodb-driver-cursor.md)
- Повертає сервер, пов'язаний із курсором

# MongoDB\Driver\Cursor::getServer

(mongodb \>=1.0.0)

MongoDB\Driver\Cursor::getServer — Повертає сервер, пов'язаний з
курсором

### Опис

final public **MongoDB\Driver\Cursor::getServer**():
[MongoDB\Driver\Server](class.mongodb-driver-server.md)

Повертає [MongoDB\Driver\Server](class.mongodb-driver-server.md),
пов'язаний із курсором. Це сервер, який виконав
[MongoDB\Driver\Query](class.mongodb-driver-query.md) або
[MongoDB\Driver\Command](class.mongodb-driver-command.md).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDB\Driver\Server](class.mongodb-driver-server.md),
пов'язаний із курсором.

### Помилки

- При помилці парсингу аргумент кидає виняток
[MongoDB\Driver\Exception\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md).

### Приклади

**Приклад #1 Приклад використання
**MongoDB\Driver\Cursor::getServer()****

` <?php$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");$query = new MongoDB\Driver\Query([]);$bulk = new MongoDB\Driver\BulkWrite; bulk->insert(['x' => 1]);$manager->executeBulkWrite('db.collection', $bulk);$cursor = $manager->executeQuery('db.collection', $query); var_dump($cursor->getServer());?> `

Результатом виконання цього прикладу буде щось подібне:

object(MongoDB\Driver\Server)#5 (10) {
["host"]=>
string(9) "localhost"
["port"]=>
int(27017)
["type"]=>
int(1)
["is_primary"]=>
bool(false)
["is_secondary"]=>
bool(false)
["is_arbiter"]=>
bool(false)
["is_hidden"]=>
bool(false)
["is_passive"]=>
bool(false)
["last_hello_response"]=>
array(8) {
["isWritablePrimary"]=>
bool(true)
["maxBsonObjectSize"]=>
int(16777216)
["maxMessageSizeBytes"]=>
int(48000000)
["maxWriteBatchSize"]=>
int(1000)
["localTime"]=>
object(MongoDB\BSON\UTCDateTime)#6 (1) {
["milliseconds"]=>
int(1446505367907)
}
["maxWireVersion"]=>
int(3)
["minWireVersion"]=>
int(0)
["ok"]=>
float(1)
}
["round_trip_time"]=>
int(584)
}

### Дивіться також

- [MongoDB\Driver\Server](class.mongodb-driver-server.md)
