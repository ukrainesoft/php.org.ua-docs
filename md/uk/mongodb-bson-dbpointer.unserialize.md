Десеріалізує DBPointer

-   [« MongoDB\\BSON\\DBPointer::\_\_toString](mongodb-bson-dbpointer.tostring.html)
    
-   [MongoDB\\BSON\\Int64 »](class.mongodb-bson-int64.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\DBPointer](class.mongodb-bson-dbpointer.html)
    
-   Десеріалізує DBPointer
    

# MongoDBBSONDBPointer::unserialize

(mongodb >=1.4.0)

MongoDBBSONDBPointer::unserialize — Десеріалізує DBPointer

### Опис

```methodsynopsis
final public MongoDB\BSON\DBPointer::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDB\\BSON\\DBPointer](class.mongodb-bson-dbpointer.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\BSON\\DBPointer::serialize()](mongodb-bson-dbpointer.serialize.html) - Серіалізує DBPointer
-   [unserialize()](function.unserialize.html) - Створює PHP-значення зі збереженого уявлення
-   [Сериализация объектов](language.oop5.serialization.html)