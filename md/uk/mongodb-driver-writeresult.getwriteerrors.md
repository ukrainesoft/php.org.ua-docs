- [« MongoDB\Driver\WriteResult::getWriteConcernError](mongodb-driver-writeresult.getwriteconcernerror.md)
- [MongoDB\Driver\WriteResult::isAcknowledged »](mongodb-driver-writeresult.isacknowledged.md)

- [PHP Manual](index.md)
- [MongoDB\Driver\WriteResult](class.mongodb-driver-writeresult.md)
- Повертає будь-які помилки запису, що відбулися

# MongoDB\Driver\WriteResult::getWriteErrors

(mongodb \>=1.0.0)

MongoDB\Driver\WriteResult::getWriteErrors — Повертає будь-які помилки
записи, що відбулися

### Опис

final public **MongoDB\Driver\WriteResult::getWriteErrors**(): array

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив об'єктів
[MongoDB\Driver\WriteError](class.mongodb-driver-writeerror.md) для
будь-яких помилок запису, виявлених під час операції запису. Масив буде
порожнім, якщо помилок не сталося.

### Помилки

- При помилці парсингу аргумент кидає виняток
[MongoDB\Driver\Exception\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md).

### Приклади

**Приклад #1 Приклад використання
**MongoDB\Driver\WriteResult::getWriteErrors()** з однією помилкою**

` <?php$manager = new MongoDB\Driver\Manager;/* За мовчанням масові операції записи виконуються послідовно по порядку * і виконання припиняється після першої . */$bulk = new MongoDB\Driver\BulkWrite;$bulk->insert(['_id' => 1]);$bulk->insert(['_id' => 2]);$bulk->insert( ['_id' => 2]);$bulk->insert(['_id' => 3]);$bulk->insert(['_id' => 4]);$bulk->insert([' _id' => 4]);try { {   $result = $manager->executeBulkWrite('db.collection', $bulk);} catch (MongoDB\Driver\Exception\BulkWriteException $e)   | ()->getWriteErrors());}?> `

Результатом виконання цього прикладу буде щось подібне:

array(1) {
[0]=>
object(MongoDB\Driver\WriteError)#5 (4) {
["message"]=>
string(81) "E11000 duplicate key error collection: db.collection index: _id_ dup key: { : 2 }"
["code"]=>
int(11000)
["index"]=>
int(2)
["info"]=>
NULL
}
}

**Приклад #2 Приклад використання
**MongoDB\Driver\WriteResult::getWriteErrors()** з кількома
помилками**

` <?php$manager = new MongoDB\Driver\Manager;/* Параметр "ordered" може використовуватися для продовження * виконання масових операцій запису після першої помилки. */$bulk = new MongoDB\Driver\BulkWrite(['ordered' =>false]);$bulk->insert(['_id' => 1]);$bulk->insert(['_id' => 2]);$bulk->insert(['_id' => 2]);$bulk->insert(['_id' => 3]);$bulk->insert(['_id' => 4] );$bulk->insert(['_id' => 4]);try {    $result = $manager->executeBulkWrite('db.collection', $bulk);} catch (MongoDB\Driver\Exception\BulkW$ e) {   var_dump($e->getWriteResult()->getWriteErrors());}?> `

Результатом виконання цього прикладу буде щось подібне:

array(2) {
[0]=>
object(MongoDB\Driver\WriteError)#5 (4) {
["message"]=>
string(81) "E11000 duplicate key error collection: db.collection index: _id_ dup key: { : 2 }"
["code"]=>
int(11000)
["index"]=>
int(2)
["info"]=>
NULL
}
[1]=>
object(MongoDB\Driver\WriteError)#6 (4) {
["message"]=>
string(81) "E11000 duplicate key error collection: db.collection index: _id_ dup key: { : 4 }"
["code"]=>
int(11000)
["index"]=>
int(5)
["info"]=>
NULL
}
}

### Дивіться також
 - [MongoDB\Driver\WriteError](class.mongodb-driver-writeerror.md)
