Десеріалізує Decimal128

-   [« MongoDB\\BSON\\Decimal128::\_\_toString](mongodb-bson-decimal128.tostring.html)
    
-   [MongoDB\\BSON\\Javascript »](class.mongodb-bson-javascript.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\Decimal128](class.mongodb-bson-decimal128.html)
    
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

Серіалізований [MongoDB\\BSON\\Decimal128](class.mongodb-bson-decimal128.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Видає виняток [MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html)якщо властивості не можуть бути десеріалізовані (наприклад, параметр `serialized` був спотворений).
-   Видає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)якщо властивості недійсні (наприклад, відсутні поля або неприпустимі значення).

### Дивіться також

-   [MongoDB\\BSON\\Decimal128::serialize()](mongodb-bson-decimal128.serialize.html) - Серіалізує Decimal128
-   [unserialize()](function.unserialize.html) - Створює PHP-значення зі збереженого уявлення
-   [Сериализация объектов](language.oop5.serialization.html)