Десеріалізує UTCDateTime

-   [« MongoDB\\BSON\\UTCDateTime::\_\_toString](mongodb-bson-utcdatetime.tostring.html)
    
-   [MongoDB\\BSON\\Type »](class.mongodb-bson-type.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\UTCDateTime](class.mongodb-bson-utcdatetime.html)
    
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

Серіалізований [MongoDB\\BSON\\UTCDateTime](class.mongodb-bson-utcdatetime.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Видає [MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html)якщо властивості не можуть бути не серіалізовані (наприклад, `serialized` був неправильно сформований).
-   Видає [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)якщо властивості неприпустимі (наприклад, відсутні поля або неприпустимі значення).

### Дивіться також

-   [MongoDB\\BSON\\UTCDateTime::serialize()](mongodb-bson-utcdatetime.serialize.html) - Серіалізує UTCDateTime
-   [unserialize()](function.unserialize.html) - Створює PHP-значення зі збереженого уявлення
-   [Сериализация объектов](language.oop5.serialization.html)