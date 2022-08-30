Десеріалізує Symbol

-   [« MongoDBBSONSymbol::toString](mongodb-bson-symbol.tostring.html)
    
-   [MongoDBBSONUndefined »](class.mongodb-bson-undefined.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBBSONSymbol](class.mongodb-bson-symbol.html)
    
-   Десеріалізує Symbol
    

# MongoDBBSONSymbol::unserialize

(mongodb >=1.4.0)

MongoDBBSONSymbol::unserialize — Десеріалізує Symbol

### Опис

```methodsynopsis
final public MongoDB\BSON\Symbol::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDBBSONSymbol](class.mongodb-bson-symbol.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBBSONSymbol::serialize()](mongodb-bson-symbol.serialize.html) - Серіалізує Symbol
-   [unserialize()](function.unserialize.md) - Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)