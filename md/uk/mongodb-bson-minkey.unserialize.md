Десеріалізує MinKey

-   [« MongoDBBSONMinKey::serialize](mongodb-bson-minkey.serialize.html)
    
-   [MongoDBBSONObjectId »](class.mongodb-bson-objectid.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBBSONMinKey](class.mongodb-bson-minkey.html)
    
-   Десеріалізує MinKey
    

# MongoDBBSONMinKey::unserialize

(mongodb >=1.2.0)

MongoDBBSONMonKey::unserialize — Десеріалізує MonKey

### Опис

```methodsynopsis
final public MongoDB\BSON\MinKey::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDBBSONMinKey](class.mongodb-bson-minkey.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBBSONMinKey::serialize()](mongodb-bson-minkey.serialize.html) - Серіалізує MinKey
-   [unserialize()](function.unserialize.md) - Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)