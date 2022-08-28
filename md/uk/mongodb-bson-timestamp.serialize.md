Серіалізує Timestamp

-   [« MongoDB\\BSON\\Timestamp::jsonSerialize](mongodb-bson-timestamp.jsonserialize.html)
    
-   [MongoDB\\BSON\\Timestamp::\_\_toString »](mongodb-bson-timestamp.tostring.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\Timestamp](class.mongodb-bson-timestamp.html)
    
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

Повертає серіалізовану виставу [MongoDB\\BSON\\Timestamp](class.mongodb-bson-timestamp.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\BSON\\Timestamp::unserialize()](mongodb-bson-timestamp.unserialize.html) - Десеріалізує Timestamp
-   [serialize()](function.serialize.html) - Генерує придатне для зберігання уявлення змінної
-   [Сериализация объектов](language.oop5.serialization.html)