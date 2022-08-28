Десеріалізує Timestamp

-   [« MongoDB\\BSON\\Timestamp::\_\_toString](mongodb-bson-timestamp.tostring.html)
    
-   [MongoDB\\BSON\\UTCDateTime »](class.mongodb-bson-utcdatetime.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\Timestamp](class.mongodb-bson-timestamp.html)
    
-   Десеріалізує Timestamp
    

# MongoDBBSONTimestamp::unserialize

(mongodb >=1.2.0)

MongoDBBSONTimestamp::unserialize — Десеріалізує Timestamp

### Опис

```methodsynopsis
final public MongoDB\BSON\Timestamp::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDB\\BSON\\Timestamp](class.mongodb-bson-timestamp.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Видає [MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html)якщо властивості не можуть бути не серіалізовані (наприклад, `serialized` був неправильно сформований).
-   Видає [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)якщо властивості неприпустимі (наприклад, відсутні поля або неприпустимі значення).

### Дивіться також

-   [MongoDB\\BSON\\Timestamp::serialize()](mongodb-bson-timestamp.serialize.html) - Серіалізує Timestamp
-   [unserialize()](function.unserialize.html) - Створює PHP-значення зі збереженого уявлення
-   [Сериализация объектов](language.oop5.serialization.html)