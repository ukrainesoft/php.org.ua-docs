---
navigation:
  - class.mongodb-driver-writeconcern.md: « MongoDB\\Driver\\WriteConcern
  - mongodb-driver-writeconcern.construct.md: 'MongoDB\\Driver\\WriteConcern::\_\_construct »'
  - index.md: PHP Manual
  - class.mongodb-driver-writeconcern.md: MongoDB\\Driver\\WriteConcern
title: 'MongoDB\\Driver\\WriteConcern::bsonSerialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\WriteConcern::bsonSerialize

(mongodb >=1.2.0)

MongoDB\\Driver\\WriteConcern::bsonSerialize — Повертає об'єкт серіалізації BSON

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteConcern::bsonSerialize(): stdClass
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт серіалізації WriteConcern як BSON.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1**MongoDB\\Driver\\WriteConcern::bsonSerialize()\*\* з більшістю гарантії запису\*\*

```php
<?php

$wc = new MongoDB\Driver\WriteConcern(MongoDB\Driver\WriteConcern::MAJORITY);
var_dump($wc->bsonSerialize());

echo "\n", MongoDB\BSON\toJSON(MongoDB\BSON\fromPHP($wc));

?>
```

Висновок наведеного прикладу буде схожим на:

```
object(stdClass)#2 (1) {
  ["w"]=>
  string(8) "majority"
}

{ "w" : "majority" }
```

**Приклад #2**MongoDB\\Driver\\WriteConcern::bsonSerialize()\*\* з часом очікування та журналом\*\*

```php
<?php

$wc = new MongoDB\Driver\WriteConcern(2, 1000, true);
var_dump($wc->bsonSerialize());

echo "\n", MongoDB\BSON\toJSON(MongoDB\BSON\fromPHP($wc));

?>
```

Висновок наведеного прикладу буде схожим на:

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

-   [MongoDB\\BSON\\Serializable::bsonSerialize()](mongodb-bson-serializable.bsonserialize.md) \- Надає масив або документ для серіалізації у BSON
-   [» Довідкова інформація щодо гарантії запису](https://www.mongodb.com/docs/manual/reference/write-concern/)
