Серіалізує Undefined

-   [« MongoDBBSONUndefined::jsonSerialize](mongodb-bson-undefined.jsonserialize.html)
    
-   [MongoDBBSONUndefined::toString »](mongodb-bson-undefined.tostring.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBBSONUndefined](class.mongodb-bson-undefined.html)
    
-   Серіалізує Undefined
    

# MongoDBBSONUndefined::serialize

(mongodb >=1.4.0)

MongoDBBSONUndefined::serialize — Серіалізує Undefined

### Опис

```methodsynopsis
final public MongoDB\BSON\Undefined::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDBBSONUndefined](class.mongodb-bson-undefined.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBBSONUndefined::unserialize()](mongodb-bson-undefined.unserialize.html) - Десеріалізує Undefined
-   [serialize()](function.serialize.html) - Генерує придатне для зберігання уявлення змінної
-   [Сериализация объектов](language.oop5.serialization.html)