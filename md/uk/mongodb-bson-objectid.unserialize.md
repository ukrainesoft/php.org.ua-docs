Десеріалізує ObjectId

-   [« MongoDB\\BSON\\ObjectId::\_\_toString](mongodb-bson-objectid.tostring.html)
    
-   [MongoDB\\BSON\\Regex »](class.mongodb-bson-regex.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\ObjectId](class.mongodb-bson-objectid.html)
    
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

Серіалізований [MongoDB\\BSON\\ObjectId](class.mongodb-bson-objectid.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Видає виняток [MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html)якщо властивості не можуть бути десеріалізовані (наприклад, `serialized` був неправильно сформований).
-   Видає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)якщо властивості недійсні (наприклад, відсутні поля або неприпустимі значення).

### Дивіться також

-   [MongoDB\\BSON\\ObjectId::serialize()](mongodb-bson-objectid.serialize.html) - Серіалізує ObjectId
-   [unserialize()](function.unserialize.html) - Створює PHP-значення зі збереженого уявлення
-   [Сериализация объектов](language.oop5.serialization.html)