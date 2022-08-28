Десеріалізує MinKey

-   [« MongoDB\\BSON\\MinKey::serialize](mongodb-bson-minkey.serialize.html)
    
-   [MongoDB\\BSON\\ObjectId »](class.mongodb-bson-objectid.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\MinKey](class.mongodb-bson-minkey.html)
    
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

Серіалізований [MongoDB\\BSON\\MinKey](class.mongodb-bson-minkey.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\BSON\\MinKey::serialize()](mongodb-bson-minkey.serialize.html) - Серіалізує MinKey
-   [unserialize()](function.unserialize.html) - Створює PHP-значення зі збереженого уявлення
-   [Сериализация объектов](language.oop5.serialization.html)