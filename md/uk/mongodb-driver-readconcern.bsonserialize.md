---
navigation:
  - class.mongodb-driver-readconcern.md: « MongoDBDriverReadConcern
  - mongodb-driver-readconcern.construct.md: 'MongoDBDriverReadConcern::construct »'
  - index.md: PHP Manual
  - class.mongodb-driver-readconcern.md: MongoDBDriverReadConcern
title: 'MongoDBDriverReadConcern::bsonSerialize'
---
# MongoDBDriverReadConcern::bsonSerialize

(mongodb >=1.2.0)

MongoDBDriverReadConcern::bsonSerialize — Повертає об'єкт для серіалізації BSON

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadConcern::bsonSerialize(): object
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт для серіалізації ReadConcern як BSON.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverReadConcern::bsonSerialize()** з порожніми гарантіями читання**

```php
<?php

$rc = new MongoDB\Driver\ReadConcern;
var_dump($rc->bsonSerialize());

echo "\n", MongoDB\BSON\toJSON(MongoDB\BSON\fromPHP($rc));

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(stdClass)#2 (0) {
}

{ }
```

**Приклад #2 Приклад використання **MongoDBDriverReadConcern::bsonSerialize()** з локальними гарантіями читання**

```php
<?php

$rc = new MongoDB\Driver\ReadConcern(MongoDB\Driver\ReadConcern::LOCAL);
var_dump($rc->bsonSerialize());

echo "\n", MongoDB\BSON\toJSON(MongoDB\BSON\fromPHP($rc));

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(stdClass)#2 (1) {
  ["level"]=>
  string(5) "local"
}

{ "level" : "local" }
```

### Дивіться також

-   [MongoDBBSONSerializable::bsonSerialize()](mongodb-bson-serializable.bsonserialize.md) - Надає масив або документ для серіалізації у BSON
-   [» Справка по гарантиям чтения](https://www.mongodb.com/docs/manual/reference/read-concern/)
