Десеріалізує Undefined

-   [« MongoDBBSONUndefined::toString](mongodb-bson-undefined.tostring.html)
    
-   [MongoDBDriverMonitoring »](mongodb.monitoring.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBBSONUndefined](class.mongodb-bson-undefined.html)
    
-   Десеріалізує Undefined
    

# MongoDBBSONUndefined::unserialize

(mongodb >=1.4.0)

MongoDBBSONUndefined::unserialize — Десеріалізує Undefined

### Опис

```methodsynopsis
final public MongoDB\BSON\Undefined::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDBBSONUndefined](class.mongodb-bson-undefined.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBBSONUndefined::serialize()](mongodb-bson-undefined.serialize.html) - Серіалізує Undefined
-   [unserialize()](function.unserialize.html) - Створює PHP-значення зі збереженого уявлення
-   [Сериализация объектов](language.oop5.serialization.html)