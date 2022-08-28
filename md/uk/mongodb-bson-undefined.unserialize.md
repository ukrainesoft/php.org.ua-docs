Десеріалізує Undefined

-   [« MongoDB\\BSON\\Undefined::\_\_toString](mongodb-bson-undefined.tostring.html)
    
-   [MongoDB\\Driver\\Monitoring »](mongodb.monitoring.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\Undefined](class.mongodb-bson-undefined.html)
    
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

Серіалізований [MongoDB\\BSON\\Undefined](class.mongodb-bson-undefined.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\BSON\\Undefined::serialize()](mongodb-bson-undefined.serialize.html) - Серіалізує Undefined
-   [unserialize()](function.unserialize.html) - Створює PHP-значення зі збереженого уявлення
-   [Сериализация объектов](language.oop5.serialization.html)