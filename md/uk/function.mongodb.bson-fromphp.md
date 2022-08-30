Повертає представлення BSON значення PHP

-   [« MongoDBBSONfromJSON](function.mongodb.bson-fromjson.html)
    
-   [MongoDBBSONtoCanonicalExtendedJSON »](function.mongodb.bson-tocanonicalextendedjson.html)
    
-   [PHP Manual](index.md)
    
-   [Функції](ref.bson.functions.md)
    
-   Повертає представлення BSON значення PHP
    

# MongoDBBSONвідPHP

(mongodb >=1.0.0)

MongoDBBSONfromPHP — Повертає представлення BSON значення PHP

### Опис

```methodsynopsis
MongoDB\BSON\fromPHP(array|object $value): string
```

Серіалізує масив або об'єкт PHP (наприклад, документ) для його подання [» BSON](https://www.mongodb.com/docs/manual/reference/bson-types/). Повернутий двійковий рядок буде описувати документ BSON.

### Список параметрів

`value` (array | об'єкт)

Значення PHP для серіалізації.

### Значення, що повертаються

Серіалізований документ BSON у вигляді двійкового рядка.

### Помилки

-   Видає [MongoDBDriverExceptionUnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html), якщо значення PHP не може бути перетворено на BSON. Можливі причини включають, але не обмежуються, зіткненням з несподіваним екземпляром [MongoDBBSONType](class.mongodb-bson-type.html) або [MongoDBBSONSerializable::bsonSerialize()](mongodb-bson-serializable.bsonserialize.html), не може повернути array або **stdClass**

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONfromPHP()****

```php
<?php

$bson = MongoDB\BSON\fromPHP(['foo' => 1]);
echo bin2hex($bson), "\n";

?>
```

Результат виконання цього прикладу:

```
0e00000010666f6f000100000000cat
```

### Дивіться також

-   [MongoDBBSONtoPHP()](function.mongodb.bson-tophp.html) - Повертає PHP подання значення BSON
-   [» MongoDB BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
-   [Постійні дані](mongodb.persistence.md)