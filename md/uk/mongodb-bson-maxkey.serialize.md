Серіалізує MaxKey

-   [« MongoDBBSONMaxKey::jsonSerialize](mongodb-bson-maxkey.jsonserialize.html)
    
-   [MongoDBBSONMaxKey::unserialize »](mongodb-bson-maxkey.unserialize.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBBSONMaxKey](class.mongodb-bson-maxkey.html)
    
-   Серіалізує MaxKey
    

# MongoDBBSONMaxKey::serialize

(mongodb >=1.2.0)

MongoDBBSONMaxKey::serialize — Серіалізує MaxKey

### Опис

```methodsynopsis
final public MongoDB\BSON\MaxKey::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDBBSONMaxKey](class.mongodb-bson-maxkey.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBBSONMaxKey::unserialize()](mongodb-bson-maxkey.unserialize.html) - Десеріалізує MaxKey
-   [serialize()](function.serialize.md) - Генерує придатне для зберігання уявлення змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)