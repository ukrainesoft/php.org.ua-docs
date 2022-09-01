---
navigation:
  - class.mongodb-driver-writeconcern.html: « MongoDBDriverWriteConcern
  - mongodb-driver-writeconcern.construct.html: 'MongoDBDriverWriteConcern::construct »'
  - index.md: PHP Manual
  - class.mongodb-driver-writeconcern.html: MongoDBDriverWriteConcern
title: 'MongoDBDriverWriteConcern::bsonSerialize'
---
# MongoDBDriverWriteConcern::bsonSerialize

(mongodb >=1.2.0)

MongoDBDriverWriteConcern::bsonSerialize — Повертає об'єкт серіалізації BSON

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteConcern::bsonSerialize(): object
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт серіалізації WriteConcern як BSON.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 **MongoDBDriverWriteConcern::bsonSerialize()** з більшістю гарантії запису**

```php
<?php

$wc = new MongoDB\Driver\WriteConcern(MongoDB\Driver\WriteConcern::MAJORITY);
var_dump($wc->bsonSerialize());

echo "\n", MongoDB\BSON\toJSON(MongoDB\BSON\fromPHP($wc));

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(stdClass)#2 (1) {
  ["w"]=>
  string(8) "majority"
}

{ "w" : "majority" }
```

**Приклад #2 **MongoDBDriverWriteConcern::bsonSerialize()** з часом очікування та журналом**

```php
<?php

$wc = new MongoDB\Driver\WriteConcern(2, 1000, true);
var_dump($wc->bsonSerialize());

echo "\n", MongoDB\BSON\toJSON(MongoDB\BSON\fromPHP($wc));

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(stdClass)#2 (3) {
  ["w"]=>
  int(2)
  ["j"]=>
  bool(true)
  ["wtimeout"]=>
  int(1000)
}

{ "w" : 2, "j" : true, "wtimeout" : 1000 }
```

### Дивіться також

-   [MongoDBBSONSerializable::bsonSerialize()](mongodb-bson-serializable.bsonserialize.html) - Надає масив або документ для серіалізації у BSON
-   [» Довідкова інформація щодо гарантії запису](https://www.mongodb.com/docs/manual/reference/write-concern/)
