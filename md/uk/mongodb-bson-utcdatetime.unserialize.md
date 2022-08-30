Десеріалізує UTCDateTime

-   [« MongoDBBSONUTCDateTime::toString](mongodb-bson-utcdatetime.tostring.html)
    
-   [MongoDBBSONType »](class.mongodb-bson-type.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBBSONUTCDateTime](class.mongodb-bson-utcdatetime.html)
    
-   Десеріалізує UTCDateTime
    

# MongoDBBSONUTCDateTime::unserialize

(mongodb >=1.2.0)

MongoDBBSONUTCDateTime::unserialize — Десеріалізує UTCDateTime

### Опис

```methodsynopsis
final public MongoDB\BSON\UTCDateTime::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDBBSONUTCDateTime](class.mongodb-bson-utcdatetime.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Видає [MongoDBDriverExceptionUnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html)якщо властивості не можуть бути не серіалізовані (наприклад, `serialized` був неправильно сформований).
-   Видає [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)якщо властивості неприпустимі (наприклад, відсутні поля або неприпустимі значення).

### Дивіться також

-   [MongoDBBSONUTCDateTime::serialize()](mongodb-bson-utcdatetime.serialize.html) - Серіалізує UTCDateTime
-   [unserialize()](function.unserialize.md) - Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)