Серіалізує DBPointer

-   [« MongoDB\\BSON\\DBPointer::jsonSerialize](mongodb-bson-dbpointer.jsonserialize.html)
    
-   [MongoDB\\BSON\\DBPointer::\_\_toString »](mongodb-bson-dbpointer.tostring.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\DBPointer](class.mongodb-bson-dbpointer.html)
    
-   Серіалізує DBPointer
    

# MongoDBBSONDBPointer::serialize

(mongodb >=1.4.0)

MongoDBBSONDBPointer::serialize — Серіалізує DBPointer

### Опис

```methodsynopsis
final public MongoDB\BSON\DBPointer::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDB\\BSON\\DBPointer](class.mongodb-bson-dbpointer.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\BSON\\DBPointer::unserialize()](mongodb-bson-dbpointer.unserialize.html) - Десеріалізує DBPointer
-   [serialize()](function.serialize.html) - Генерує придатне для зберігання подання змінної
-   [Сериализация объектов](language.oop5.serialization.html)