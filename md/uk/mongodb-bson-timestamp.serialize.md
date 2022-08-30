Серіалізує Timestamp

-   [« MongoDBBSONTimestamp::jsonSerialize](mongodb-bson-timestamp.jsonserialize.html)
    
-   [MongoDBBSONTimestamp::toString »](mongodb-bson-timestamp.tostring.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBBSONTimestamp](class.mongodb-bson-timestamp.html)
    
-   Серіалізує Timestamp
    

# MongoDBBSONTimestamp::serialize

(mongodb >=1.2.0)

MongoDBBSONTimestamp::serialize — Серіалізує Timestamp

### Опис

```methodsynopsis
final public MongoDB\BSON\Timestamp::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDBBSONTimestamp](class.mongodb-bson-timestamp.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBBSONTimestamp::unserialize()](mongodb-bson-timestamp.unserialize.html) - Десеріалізує Timestamp
-   [serialize()](function.serialize.html) - Генерує придатне для зберігання уявлення змінної
-   [Сериализация объектов](language.oop5.serialization.html)