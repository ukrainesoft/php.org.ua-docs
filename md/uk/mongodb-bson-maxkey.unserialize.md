Десеріалізує MaxKey

-   [« MongoDBBSONMaxKey::serialize](mongodb-bson-maxkey.serialize.html)
    
-   [MongoDBBSONMinKey »](class.mongodb-bson-minkey.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBBSONMaxKey](class.mongodb-bson-maxkey.html)
    
-   Десеріалізує MaxKey
    

# MongoDBBSONMaxKey::unserialize

(mongodb >=1.2.0)

MongoDBBSONMaxKey::unserialize — Десеріалізує MaxKey

### Опис

```methodsynopsis
final public MongoDB\BSON\MaxKey::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDBBSONMaxKey](class.mongodb-bson-maxkey.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBBSONMaxKey::serialize()](mongodb-bson-maxkey.serialize.html) - Серіалізує MaxKey
-   [unserialize()](function.unserialize.html) - Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.html)