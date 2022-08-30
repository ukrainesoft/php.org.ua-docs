Серіалізує ServerApi

-   [« MongoDBDriverServerApi::construct](mongodb-driver-serverapi.construct.html)
    
-   [MongoDBDriverServerApi::unserialize »](mongodb-driver-serverapi.unserialize.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverServerApi](class.mongodb-driver-serverapi.html)
    
-   Серіалізує ServerApi
    

# MongoDBDriverServerApi::serialize

(mongodb >=1.10.0)

MongoDBDriverServerApi::serialize — Серіалізує ServerApi

### Опис

```methodsynopsis
final public MongoDB\Driver\ServerApi::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDBDriverServerApi](class.mongodb-driver-serverapi.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverServerApi::unserialize()](mongodb-driver-serverapi.unserialize.html) - Десеріалізує ServerApi
-   [serialize()](function.serialize.md) - Генерує придатне для зберігання уявлення змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)