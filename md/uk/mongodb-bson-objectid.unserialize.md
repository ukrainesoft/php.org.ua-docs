Десеріалізує ObjectId

-   [« MongoDBBSONObjectId::toString](mongodb-bson-objectid.tostring.html)
    
-   [MongoDBBSONRegex »](class.mongodb-bson-regex.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBBSONObjectId](class.mongodb-bson-objectid.html)
    
-   Десеріалізує ObjectId
    

# MongoDBBSONObjectId::unserialize

(mongodb >=1.2.0)

MongoDBBSONObjectId::unserialize — Десеріалізує ObjectId

### Опис

```methodsynopsis
final public MongoDB\BSON\ObjectId::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDBBSONObjectId](class.mongodb-bson-objectid.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Видає виняток [MongoDBDriverExceptionUnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html)якщо властивості не можуть бути десеріалізовані (наприклад, `serialized` був неправильно сформований).
-   Видає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)якщо властивості недійсні (наприклад, відсутні поля або неприпустимі значення).

### Дивіться також

-   [MongoDBBSONObjectId::serialize()](mongodb-bson-objectid.serialize.html) - Серіалізує ObjectId
-   [unserialize()](function.unserialize.md) - Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)