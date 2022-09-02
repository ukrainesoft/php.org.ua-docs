---
navigation:
  - class.mongodb-driver-readpreference.md: « MongoDBDriverReadPreference
  - mongodb-driver-readpreference.construct.md: 'MongoDBDriverReadPreference::construct »'
  - index.md: PHP Manual
  - class.mongodb-driver-readpreference.md: MongoDBDriverReadPreference
title: 'MongoDBDriverReadPreference::bsonSerialize'
---
# MongoDBDriverReadPreference::bsonSerialize

(mongodb >=1.2.0)

MongoDBDriverReadPreference::bsonSerialize — Повертає об'єкт серіалізації BSON

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadPreference::bsonSerialize(): object
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт серіалізації ReadPreference як BSON.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverReadPreference::bsonSerialize()** з первинною перевагою читання**

```php
<?php

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_PRIMARY);
var_dump($rp->bsonSerialize());

echo "\n", MongoDB\BSON\toJSON(MongoDB\BSON\fromPHP($rp));

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(stdClass)#2 (1) {
  ["mode"]=>
  string(7) "primary"
}

{ "mode" : "primary" }
```

**Приклад #2 Приклад використання **MongoDBDriverReadPreference::bsonSerialize()** з вторинною перевагою читання та наборами тегів**

```php
<?php

$rp = new MongoDB\Driver\ReadPreference(
    MongoDB\Driver\ReadPreference::RP_SECONDARY,
    [
        ['dc' => 'ny'],
        ['dc' => 'sf', 'use' => 'reporting'],
        []
    ]
);
var_dump($rp->bsonSerialize());

echo "\n", MongoDB\BSON\toJSON(MongoDB\BSON\fromPHP($rp));

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
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

{ "mode" : "secondary", "tags" : [ { "dc" : "ny" }, { "dc" : "sf", "use" : "reporting" }, {  } ] }
```

**Приклад #3 Приклад використання **MongoDBDriverReadPreference::bsonSerialize()** з вторинною перевагою читання та максимальним staleness**

```php
<?php

$rp = new MongoDB\Driver\ReadPreference(
    MongoDB\Driver\ReadPreference::RP_SECONDARY,
    null,
    ['maxStalenessSeconds' => 120]
);
var_dump($rp->bsonSerialize());

echo "\n", MongoDB\BSON\toJSON(MongoDB\BSON\fromPHP($rp));

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(stdClass)#2 (2) {
  ["mode"]=>
  string(9) "secondary"
  ["maxStalenessSeconds"]=>
  int(120)
}

{ "mode" : "secondary", "maxStalenessSeconds" : 120 }
```

### Дивіться також

-   [MongoDBBSONSerializable::bsonSerialize()](mongodb-bson-serializable.bsonserialize.md) - Надає масив або документ для серіалізації у BSON
-   [» Справочная информация по предпочтению чтения](https://www.mongodb.com/docs/manual/core/read-preference/)
