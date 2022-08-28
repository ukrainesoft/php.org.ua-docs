Повертає об'єкт для серіалізації BSON

-   [« MongoDB\\Driver\\ReadConcern](class.mongodb-driver-readconcern.html)
    
-   [MongoDB\\Driver\\ReadConcern::\_\_construct »](mongodb-driver-readconcern.construct.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\ReadConcern](class.mongodb-driver-readconcern.html)
    
-   Повертає об'єкт для серіалізації BSON
    

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

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverReadConcern::bsonSerialize()** з порожніми гарантіями читання**

```php
<?php

$rc = new MongoDB\Driver\ReadConcern;
var_dump($rc->bsonSerialize());

echo "\n", MongoDB\BSON\toJSON(MongoDB\BSON\fromPHP($rc));

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

$rc = new MongoDB\Driver\ReadConcern(MongoDB\Driver\ReadConcern::LOCAL);
var_dump($rc->bsonSerialize());

echo "\n", MongoDB\BSON\toJSON(MongoDB\BSON\fromPHP($rc));

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

-   [MongoDB\\BSON\\Serializable::bsonSerialize()](mongodb-bson-serializable.bsonserialize.html) - Надає масив або документ для серіалізації у BSON
-   [» Справка по гарантиям чтения](https://www.mongodb.com/docs/manual/reference/read-concern/)