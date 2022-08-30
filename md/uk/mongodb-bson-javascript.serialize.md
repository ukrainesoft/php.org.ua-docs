Серіалізувати JavaScript

-   [« MongoDBBSONJavascript::jsonSerialize](mongodb-bson-javascript.jsonserialize.html)
    
-   [MongoDBBSONJavascript::toString »](mongodb-bson-javascript.tostring.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBBSONJavascript](class.mongodb-bson-javascript.html)
    
-   Серіалізувати JavaScript
    

# MongoDBBSONJavascript::serialize

(mongodb >=1.2.0)

MongoDBBSONJavascript::serialize — Серіалізувати JavaScript

### Опис

```methodsynopsis
final public MongoDB\BSON\Javascript::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDBBSONJavascript](class.mongodb-bson-javascript.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBBSONJavascript::unserialize()](mongodb-bson-javascript.unserialize.html) - Десеріалізувати JavaScript
-   [serialize()](function.serialize.md) - Генерує придатне для зберігання подання змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)