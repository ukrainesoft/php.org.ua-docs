Десеріалізація CursorId

-   [« MongoDBDriverCursorId::toString](mongodb-driver-cursorid.tostring.html)
    
-   [MongoDBDriverCursorInterface »](class.mongodb-driver-cursorinterface.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverCursorId](class.mongodb-driver-cursorid.html)
    
-   Десеріалізація CursorId
    

# MongoDBDriverCursorId::unserialize

(mongodb >=1.7.0)

MongoDBDriverCursorId::unserialize — Десеріалізація CursorId

### Опис

```methodsynopsis
final public MongoDB\Driver\CursorId::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDBDriverCursorId](class.mongodb-driver-cursorid.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Кидає виняток [MongoDBDriverExceptionUnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html) якщо виникла неможливо зробити десеріалізацію властивості, наприклад, якщо значення `serialized` не коректно.
-   Кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html) якщо властивості не коректні, наприклад, пропущені поля або вони мають некоректні значення.

### Дивіться також

-   [MongoDBDriverCursorId::serialize()](mongodb-driver-cursorid.serialize.html) - Серіалізація CursorId
-   [unserialize()](function.unserialize.html) - Створює PHP-значення зі збереженого уявлення
-   [Сериализация объектов](language.oop5.serialization.html)