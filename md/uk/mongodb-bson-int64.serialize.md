Серіалізує Int64

-   [« MongoDB\\BSON\\Int64::jsonSerialize](mongodb-bson-int64.jsonserialize.html)
    
-   [MongoDB\\BSON\\Int64::\_\_toString »](mongodb-bson-int64.tostring.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\Int64](class.mongodb-bson-int64.html)
    
-   Серіалізує Int64
    

# MongoDBBSONInt64::serialize

(mongodb >=1.5.0)

MongoDBBSONInt64::serialize — Серіалізує Int64

### Опис

```methodsynopsis
final public MongoDB\BSON\Int64::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDB\\BSON\\Int64](class.mongodb-bson-int64.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\BSON\\Int64::unserialize()](mongodb-bson-int64.unserialize.html) - Десеріалізує Int64
-   [serialize()](function.serialize.html) - Генерує придатне для зберігання подання змінної
-   [Сериализация объектов](language.oop5.serialization.html)