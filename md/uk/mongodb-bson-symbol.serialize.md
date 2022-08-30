Серіалізує Symbol

-   [« MongoDBBSONSymbol::jsonSerialize](mongodb-bson-symbol.jsonserialize.html)
    
-   [MongoDBBSONSymbol::toString »](mongodb-bson-symbol.tostring.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBBSONSymbol](class.mongodb-bson-symbol.html)
    
-   Серіалізує Symbol
    

# MongoDBBSONSymbol::serialize

(mongodb >=1.4.0)

MongoDBBSONSymbol::serialize — Серіалізує Symbol

### Опис

```methodsynopsis
final public MongoDB\BSON\Symbol::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDBBSONSymbol](class.mongodb-bson-symbol.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBBSONSymbol::unserialize()](mongodb-bson-symbol.unserialize.html) - Десеріалізує Symbol
-   [serialize()](function.serialize.md) - Генерує придатне для зберігання подання змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)