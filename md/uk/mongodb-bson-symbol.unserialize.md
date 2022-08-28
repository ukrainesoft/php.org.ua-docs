Десеріалізує Symbol

-   [« MongoDB\\BSON\\Symbol::\_\_toString](mongodb-bson-symbol.tostring.html)
    
-   [MongoDB\\BSON\\Undefined »](class.mongodb-bson-undefined.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\Symbol](class.mongodb-bson-symbol.html)
    
-   Десеріалізує Symbol
    

# MongoDBBSONSymbol::unserialize

(mongodb >=1.4.0)

MongoDBBSONSymbol::unserialize — Десеріалізує Symbol

### Опис

```methodsynopsis
final public MongoDB\BSON\Symbol::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDB\\BSON\\Symbol](class.mongodb-bson-symbol.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\BSON\\Symbol::serialize()](mongodb-bson-symbol.serialize.html) - Серіалізує Symbol
-   [unserialize()](function.unserialize.html) - Створює PHP-значення зі збереженого уявлення
-   [Сериализация объектов](language.oop5.serialization.html)