Десеріалізує Binary

-   [« MongoDB\\BSON\\Binary::\_\_toString](mongodb-bson-binary.tostring.html)
    
-   [MongoDB\\BSON\\Decimal128 »](class.mongodb-bson-decimal128.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\Binary](class.mongodb-bson-binary.html)
    
-   Десеріалізує Binary
    

# MongoDBBSONBinary::unserialize

(mongodb >=1.2.0)

MongoDBBSONBinary::unserialize — Десеріалізує Binary

### Опис

```methodsynopsis
final public MongoDB\BSON\Binary::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDB\\BSON\\Binary](class.mongodb-bson-binary.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Видає [MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html)якщо властивості не можуть бути десеріалізовані (наприклад, `serialized` був неправильно сформований).
-   Видає [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)якщо властивості неприпустимі (наприклад, відсутні поля або неприпустимі значення).

### Дивіться також

-   [MongoDB\\BSON\\Binary::serialize()](mongodb-bson-binary.serialize.html) - Серіалізує Binary
-   [unserialize()](function.unserialize.html) - Створює PHP-значення зі збереженого уявлення
-   [Сериализация объектов](language.oop5.serialization.html)