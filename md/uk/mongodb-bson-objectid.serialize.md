Серіалізує ObjectId

-   [« MongoDB\\BSON\\ObjectId::jsonSerialize](mongodb-bson-objectid.jsonserialize.html)
    
-   [MongoDB\\BSON\\ObjectId::\_\_toString »](mongodb-bson-objectid.tostring.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\ObjectId](class.mongodb-bson-objectid.html)
    
-   Серіалізує ObjectId
    

# MongoDBBSONObjectId::serialize

(mongodb >=1.2.0)

MongoDBBSONObjectId::serialize — Серіалізує ObjectId

### Опис

```methodsynopsis
final public MongoDB\BSON\ObjectId::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDB\\BSON\\ObjectId](class.mongodb-bson-objectid.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\BSON\\ObjectId::unserialize()](mongodb-bson-objectid.unserialize.html) - Десеріалізує ObjectId
-   [serialize()](function.serialize.html) - Генерує придатне для зберігання подання змінної
-   [Сериализация объектов](language.oop5.serialization.html)