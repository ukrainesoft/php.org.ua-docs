Десеріалізація WriteConcern

-   [« MongoDBDriverWriteConcern::serialize](mongodb-driver-writeconcern.serialize.html)
    
-   [MongoDBDriverReadPreference »](class.mongodb-driver-readpreference.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverWriteConcern](class.mongodb-driver-writeconcern.html)
    
-   Десеріалізація WriteConcern
    

# MongoDBDriverWriteConcern::unserialize

(mongodb >=1.7.0)

MongoDBDriverWriteConcern::unserialize — Десеріалізація WriteConcern

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteConcern::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDBDriverWriteConcern](class.mongodb-driver-writeconcern.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Кидає виняток [MongoDBDriverExceptionUnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html) якщо виникла неможливо зробити десеріалізацію властивості, наприклад, якщо значення `serialized` не коректно.
-   Кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html) якщо властивості не коректні, наприклад, пропущені поля або вони мають некоректні значення.

### Дивіться також

-   [MongoDBDriverWriteConcern::serialize()](mongodb-driver-writeconcern.serialize.html) - Серіалізація WriteConcern
-   [unserialize()](function.unserialize.html) - Створює PHP-значення зі збереженого уявлення
-   [Сериализация объектов](language.oop5.serialization.html)