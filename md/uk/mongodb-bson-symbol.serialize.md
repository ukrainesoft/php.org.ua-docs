Серіалізує Symbol

-   [« MongoDB\\BSON\\Symbol::jsonSerialize](mongodb-bson-symbol.jsonserialize.html)
    
-   [MongoDB\\BSON\\Symbol::\_\_toString »](mongodb-bson-symbol.tostring.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\Symbol](class.mongodb-bson-symbol.html)
    
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

Повертає серіалізовану виставу [MongoDB\\BSON\\Symbol](class.mongodb-bson-symbol.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\BSON\\Symbol::unserialize()](mongodb-bson-symbol.unserialize.html) - Десеріалізує Symbol
-   [serialize()](function.serialize.html) - Генерує придатне для зберігання подання змінної
-   [Сериализация объектов](language.oop5.serialization.html)