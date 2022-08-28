Серіалізує Undefined

-   [« MongoDB\\BSON\\Undefined::jsonSerialize](mongodb-bson-undefined.jsonserialize.html)
    
-   [MongoDB\\BSON\\Undefined::\_\_toString »](mongodb-bson-undefined.tostring.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\Undefined](class.mongodb-bson-undefined.html)
    
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

Повертає серіалізовану виставу [MongoDB\\BSON\\Undefined](class.mongodb-bson-undefined.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\BSON\\Undefined::unserialize()](mongodb-bson-undefined.unserialize.html) - Десеріалізує Undefined
-   [serialize()](function.serialize.html) - Генерує придатне для зберігання уявлення змінної
-   [Сериализация объектов](language.oop5.serialization.html)