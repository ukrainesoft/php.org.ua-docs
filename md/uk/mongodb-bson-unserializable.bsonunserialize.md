Створює об'єкт із масиву BSON або документа

-   [« MongoDBBSONUnserializable](class.mongodb-bson-unserializable.html)
    
-   [MongoDBBSONBinaryInterface »](class.mongodb-bson-binaryinterface.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBBSONUnserializable](class.mongodb-bson-unserializable.html)
    
-   Створює об'єкт із масиву BSON або документа
    

# MongoDBBSONUnserializable::bsonUnserialize

(mongodb >=1.0.0)

MongoDBBSONUnserializable::bsonUnserialize — Створює об'єкт із масиву BSON або документа

### Опис

```methodsynopsis
abstract public MongoDB\BSON\Unserializable::bsonUnserialize(array $data): void
```

Викликається під час десеріалізації об'єкта із BSON. Властивості масиву BSON або документа будуть передані методом у вигляді масиву (array).

Не забудьте перевірити властивість id під час обробки даних із документа BSON.

> **Зауваження**: Даний метод служить як [конструктора](language.oop5.decon.html#language.oop5.decon.constructor) об'єкта Метод [construct()](language.oop5.decon.html#object.construct) *не* буде викликатись після цього методу.

### Список параметрів

`data` (array)

Властивості в масиві BSON або документі.

### Значення, що повертаються

Значення цього методу, що повертається, ігнорується.

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONUnserializable::bsonUnserialize()****

```php
<?php

class MyDocument implements MongoDB\BSON\Unserializable
{
    private $data = [];

    function bsonUnserialize(array $data): void
    {
        $this->data = $data;
    }
}

$bson = MongoDB\BSON\fromJSON('{ "foo": "bar" }');
$value = MongoDB\BSON\toPHP($bson, ['root' => 'MyDocument']);
var_dump($value);

?>
```

Результат виконання цього прикладу:

```
object(MyDocument)#1 (1) {
  ["data":"MyDocument":private]=>
  array(1) {
    ["foo"]=>
    string(3) "bar"
  }
}
```

### Дивіться також

-   [MongoDBBSONSerializable::bsonSerialize()](mongodb-bson-serializable.bsonserialize.html) - Надає масив або документ для серіалізації у BSON
-   [MongoDBBSONPersistable](class.mongodb-bson-persistable.html)
-   [Постійні дані](mongodb.persistence.md)