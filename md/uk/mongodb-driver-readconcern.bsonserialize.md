---
navigation:
  - class.mongodb-driver-readconcern.md: « MongoDB\\Driver\\ReadConcern
  - mongodb-driver-readconcern.construct.md: 'MongoDB\\Driver\\ReadConcern::\_\_construct »'
  - index.md: PHP Manual
  - class.mongodb-driver-readconcern.md: MongoDB\\Driver\\ReadConcern
title: 'MongoDB\\Driver\\ReadConcern::bsonSerialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ReadConcern::bsonSerialize

(mongodb >=1.2.0)

MongoDB\\Driver\\ReadConcern::bsonSerialize — Повертає об'єкт для серіалізації BSON

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadConcern::bsonSerialize(): stdClass
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт для серіалізації ReadConcern як BSON.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Пример #1 Пример использования**MongoDB\\Driver\\ReadConcern::bsonSerialize()\*\* з порожніми гарантіями читання\*\*

```php
<?php

$rc = new MongoDB\Driver\ReadConcern;
var_dump($rc->bsonSerialize());

echo "\n", MongoDB\BSON\toJSON(MongoDB\BSON\fromPHP($rc));

?>
```

Висновок наведеного прикладу буде схожим на:

```
object(stdClass)#2 (0) {
}

{ }
```

**Пример #2 Пример использования**MongoDB\\Driver\\ReadConcern::bsonSerialize()\*\* з локальними гарантіями читання\*\*

```php
<?php

$rc = new MongoDB\Driver\ReadConcern(MongoDB\Driver\ReadConcern::LOCAL);
var_dump($rc->bsonSerialize());

echo "\n", MongoDB\BSON\toJSON(MongoDB\BSON\fromPHP($rc));

?>
```

Висновок наведеного прикладу буде схожим на:

```
object(stdClass)#2 (1) {
  ["level"]=>
  string(5) "local"
}

{ "level" : "local" }
```

### Дивіться також

-   [MongoDB\\BSON\\Serializable::bsonSerialize()](mongodb-bson-serializable.bsonserialize.md) \- Надає масив або документ для серіалізації у BSON
-   [» Довідка за гарантіями читання](https://www.mongodb.com/docs/manual/reference/read-concern/)
