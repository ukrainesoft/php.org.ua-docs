---
navigation:
  - class.mongodb-bson-unserializable.md: « MongoDB\\BSON\\Unserializable
  - class.mongodb-bson-binaryinterface.md: MongoDB\\BSON\\BinaryInterface »
  - index.md: PHP Manual
  - class.mongodb-bson-unserializable.md: MongoDB\\BSON\\Unserializable
title: 'MongoDB\\BSON\\Unserializable::bsonUnserialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Unserializable::bsonUnserialize

(mongodb >=1.0.0)

MongoDB\\BSON\\Unserializable::bsonUnserialize — Створює об'єкт із масиву BSON або документа

### Опис

```methodsynopsis
abstract public MongoDB\BSON\Unserializable::bsonUnserialize(array $data): void
```

Викликається під час десеріалізації об'єкта із BSON. Властивості масиву BSON або документа будуть передані методом у вигляді масиву (array).

Не забудьте проверить свойство\_id під час обробки даних із документа BSON.

> **Зауваження**: Даний метод служить як [конструктора](language.oop5.decon.md#language.oop5.decon.constructor) об'єкта Метод [\_\_construct()](language.oop5.decon.md#object.construct) *не* буде викликатись після цього методу.

### Список параметрів

`data`(array)

Властивості в масиві BSON або документі.

### Значення, що повертаються

Значення цього методу, що повертається, ігнорується.

### Приклади

**Пример #1 Пример использования**MongoDB\\BSON\\Unserializable::bsonUnserialize()\*\*\*\*

```php
<?php

class MyDocument implements MongoDB\BSON\Unserializable
{
    private $data = [];

    function bsonUnserialize(array $data): void
    {
        $this->data = $data;
    }
}

$bson = MongoDB\BSON\fromJSON('{ "foo": "bar" }');
$value = MongoDB\BSON\toPHP($bson, ['root' => 'MyDocument']);
var_dump($value);

?>
```

Результат виконання наведеного прикладу:

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

-   [MongoDB\\BSON\\Serializable::bsonSerialize()](mongodb-bson-serializable.bsonserialize.md) \- Надає масив або документ для серіалізації у BSON
-   [MongoDB\\BSON\\Persistable](class.mongodb-bson-persistable.md)
-   [Постійні дані](mongodb.persistence.md)
