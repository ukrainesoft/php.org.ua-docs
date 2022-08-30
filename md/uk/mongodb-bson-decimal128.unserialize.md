Десеріалізує Decimal128

-   [« MongoDBBSONDecimal128::toString](mongodb-bson-decimal128.tostring.html)
    
-   [MongoDBBSONJavascript »](class.mongodb-bson-javascript.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBBSONDecimal128](class.mongodb-bson-decimal128.html)
    
-   Десеріалізує Decimal128
    

# MongoDBBSONDecimal128::unserialize

(mongodb >=1.2.0)

MongoDBBSONDecimal128::unserialize — Десеріалізує Decimal128

### Опис

```methodsynopsis
final public MongoDB\BSON\Decimal128::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDBBSONDecimal128](class.mongodb-bson-decimal128.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Видає виняток [MongoDBDriverExceptionUnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html)якщо властивості не можуть бути десеріалізовані (наприклад, параметр `serialized` був спотворений).
-   Видає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)якщо властивості недійсні (наприклад, відсутні поля або неприпустимі значення).

### Дивіться також

-   [MongoDBBSONDecimal128::serialize()](mongodb-bson-decimal128.serialize.html) - Серіалізує Decimal128
-   [unserialize()](function.unserialize.md) - Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)