- [« MongoDB\Driver\ReadPreference](class.mongodb-driver-readpreference.md)
- [MongoDB\Driver\ReadPreference::\_\_construct »](mongodb-driver-readpreference.construct.md)

- [PHP Manual](index.md)
- [MongoDB\Driver\ReadPreference](class.mongodb-driver-readpreference.md)
- Повертає об'єкт серіалізації BSON

# MongoDB\Driver\ReadPreference::bsonSerialize

(mongodb \>=1.2.0)

MongoDB\Driver\ReadPreference::bsonSerialize — Повертає об'єкт
серіалізації BSON

### Опис

final public **MongoDB\Driver\ReadPreference::bsonSerialize**(): object

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт серіалізації ReadPreference як BSON.

### Помилки

- При помилці парсингу аргумент кидає виняток
[MongoDB\Driver\Exception\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md).

### Приклади

**Приклад #1 Приклад використання
**MongoDB\Driver\ReadPreference::bsonSerialize()** з первинним
перевагою читання**

` <?php$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_PRIMARY);var_dump($rp->bsonSerialize());echo "
", MongoDB\BSON oJSON(MongoDB\BSON romPHP($rp));?> `

Результатом виконання цього прикладу буде щось подібне:

object(stdClass)#2 (1) {
["mode"]=>
string(7) "primary"
}

{ "mode" : "primary" }

**Приклад #2 Приклад використання
**MongoDB\Driver\ReadPreference::bsonSerialize()** з вторинним
перевагою читання та наборами тегів**

`<?php$rp = new MongoDB\Driver\ReadPreference(  MongoDB\Driver\ReadPreference::RP_SECONDARY,   ['d='              'reporting'],        []    ]);var_dump($rp->bsonSerialize());echo "
", MongoDB\BSON oJSON(MongoDB\BSON romPHP($rp));?> `

Результатом виконання цього прикладу буде щось подібне:

object(stdClass)#2 (2) {
["mode"]=>
string(9) "secondary"
["tags"]=>
array(3) {
[0]=>
object(stdClass)#1 (1) {
["dc"]=>
string(2) "ny"
}
[1]=>
object(stdClass)#5 (2) {
["dc"]=>
string(2) "sf"
["use"]=>
string(9) "reporting"
}
[2]=>
object(stdClass)#4 (0) {
}
}
}

{ "mode" : "secondary", "tags" : [ { "dc" : "ny" }, { "dc" : "sf", "use" : "reporting" }, { } ] }

**Приклад #3 Приклад використання
**MongoDB\Driver\ReadPreference::bsonSerialize()** з вторинним
перевагою читання та максимальним staleness**

`<?php$rp = new MongoDB\Driver\ReadPreference(  MongoDB\Driver\ReadPreference::RP_SECONDARY,   null,    ['maxStalenessSeconds')=>|
", MongoDB\BSON oJSON(MongoDB\BSON romPHP($rp));?> `

Результатом виконання цього прикладу буде щось подібне:

object(stdClass)#2 (2) {
["mode"]=>
string(9) "secondary"
["maxStalenessSeconds"]=>
int(120)
}

{ "mode" : "secondary", "maxStalenessSeconds" : 120 }

### Дивіться також

- [MongoDB\BSON\Serializable::bsonSerialize()](mongodb-bson-serializable.bsonserialize.md) -
Надає масив або документ для серіалізації у BSON
- [» Довідкова інформація за перевагою читання](https://www.mongodb.com/docs/manual/core/read-preference/)
