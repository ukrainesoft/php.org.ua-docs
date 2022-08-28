Серіалізує UTCDateTime

-   [« MongoDB\\BSON\\UTCDateTime::jsonSerialize](mongodb-bson-utcdatetime.jsonserialize.html)
    
-   [MongoDB\\BSON\\UTCDateTime::toDateTime »](mongodb-bson-utcdatetime.todatetime.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\UTCDateTime](class.mongodb-bson-utcdatetime.html)
    
-   Серіалізує UTCDateTime
    

# MongoDBBSONUTCDateTime::serialize

(mongodb >=1.2.0)

MongoDBBSONUTCDateTime::serialize — Серіалізує UTCDateTime

### Опис

```methodsynopsis
final public MongoDB\BSON\UTCDateTime::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDB\\BSON\\UTCDateTime](class.mongodb-bson-utcdatetime.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\BSON\\UTCDateTime::unserialize()](mongodb-bson-utcdatetime.unserialize.html) - Десеріалізує UTCDateTime
-   [serialize()](function.serialize.html) - Генерує придатне для зберігання подання змінної
-   [Сериализация объектов](language.oop5.serialization.html)