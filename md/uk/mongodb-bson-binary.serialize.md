Серіалізує Binary

-   [« MongoDB\\BSON\\Binary::jsonSerialize](mongodb-bson-binary.jsonserialize.html)
    
-   [MongoDB\\BSON\\Binary::\_\_toString »](mongodb-bson-binary.tostring.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\Binary](class.mongodb-bson-binary.html)
    
-   Серіалізує Binary
    

# MongoDBBSONBinary::serialize

(mongodb >=1.2.0)

MongoDBBSONBinary::serialize — Серіалізує Binary

### Опис

```methodsynopsis
final public MongoDB\BSON\Binary::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDB\\BSON\\Binary](class.mongodb-bson-binary.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\BSON\\Binary::unserialize()](mongodb-bson-binary.unserialize.html) - Десеріалізує Binary
-   [serialize()](function.serialize.html) - Генерує придатне для зберігання уявлення змінної
-   [Сериализация объектов](language.oop5.serialization.html)