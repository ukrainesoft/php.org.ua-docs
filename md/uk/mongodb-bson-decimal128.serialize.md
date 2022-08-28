Серіалізує Decimal128

-   [« MongoDB\\BSON\\Decimal128::jsonSerialize](mongodb-bson-decimal128.jsonserialize.html)
    
-   [MongoDB\\BSON\\Decimal128::\_\_toString »](mongodb-bson-decimal128.tostring.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\Decimal128](class.mongodb-bson-decimal128.html)
    
-   Серіалізує Decimal128
    

# MongoDBBSONDecimal128::serialize

(mongodb >=1.2.0)

MongoDBBSONDecimal128::serialize — Серіалізує Decimal128

### Опис

```methodsynopsis
final public MongoDB\BSON\Decimal128::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDB\\BSON\\Decimal128](class.mongodb-bson-decimal128.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\BSON\\Decimal128::unserialize()](mongodb-bson-decimal128.unserialize.html) - Десеріалізує Decimal128
-   [serialize()](function.serialize.html) - Генерує придатне для зберігання подання змінної
-   [Сериализация объектов](language.oop5.serialization.html)