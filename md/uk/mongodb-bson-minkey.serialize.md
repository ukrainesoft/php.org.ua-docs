Серіалізує MinKey

-   [« MongoDB\\BSON\\MinKey::jsonSerialize](mongodb-bson-minkey.jsonserialize.html)
    
-   [MongoDB\\BSON\\MinKey::unserialize »](mongodb-bson-minkey.unserialize.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\MinKey](class.mongodb-bson-minkey.html)
    
-   Серіалізує MinKey
    

# MongoDBBSONMinKey::serialize

(mongodb >=1.2.0)

MongoDBBSONMonKey::serialize — Серіалізує MonKey

### Опис

```methodsynopsis
final public MongoDB\BSON\MinKey::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDB\\BSON\\MinKey](class.mongodb-bson-minkey.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\BSON\\MinKey::unserialize()](mongodb-bson-minkey.unserialize.html) - Десеріалізує MinKey
-   [serialize()](function.serialize.html) - Генерує придатне для зберігання подання змінної
-   [Сериализация объектов](language.oop5.serialization.html)