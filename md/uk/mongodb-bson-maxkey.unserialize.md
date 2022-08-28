Десеріалізує MaxKey

-   [« MongoDB\\BSON\\MaxKey::serialize](mongodb-bson-maxkey.serialize.html)
    
-   [MongoDB\\BSON\\MinKey »](class.mongodb-bson-minkey.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\MaxKey](class.mongodb-bson-maxkey.html)
    
-   Десеріалізує MaxKey
    

# MongoDBBSONMaxKey::unserialize

(mongodb >=1.2.0)

MongoDBBSONMaxKey::unserialize — Десеріалізує MaxKey

### Опис

```methodsynopsis
final public MongoDB\BSON\MaxKey::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDB\\BSON\\MaxKey](class.mongodb-bson-maxkey.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\BSON\\MaxKey::serialize()](mongodb-bson-maxkey.serialize.html) - Серіалізує MaxKey
-   [unserialize()](function.unserialize.html) - Створює PHP-значення зі збереженого уявлення
-   [Сериализация объектов](language.oop5.serialization.html)