Десеріалізувати JavaScript

-   [« MongoDBBSONJavascript::toString](mongodb-bson-javascript.tostring.html)
    
-   [MongoDBBSONMaxKey »](class.mongodb-bson-maxkey.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBBSONJavascript](class.mongodb-bson-javascript.html)
    
-   Десеріалізувати JavaScript
    

# MongoDBBSONJavascript::unserialize

(mongodb >=1.2.0)

MongoDBBSONJavascript::unserialize — Десеріалізувати JavaScript

### Опис

```methodsynopsis
final public MongoDB\BSON\Javascript::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDBBSONJavascript](class.mongodb-bson-javascript.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Викидає [MongoDBDriverExceptionUnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html)якщо властивості не можуть бути десеріалізовані (тобто . `serialized` неправильний).
-   Викидає [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html), якщо властивості некоректні (наприклад, відсутні поля чи неправильні неправильні значення).

### Дивіться також

-   [MongoDBBSONJavascript::serialize()](mongodb-bson-javascript.serialize.html) - Серіалізувати JavaScript
-   [unserialize()](function.unserialize.html) - Створює PHP-значення зі збереженого уявлення
-   [Сериализация объектов](language.oop5.serialization.html)