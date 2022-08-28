Десеріалізує Int64

-   [« MongoDB\\BSON\\Int64::\_\_toString](mongodb-bson-int64.tostring.html)
    
-   [MongoDB\\BSON\\Symbol »](class.mongodb-bson-symbol.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\Int64](class.mongodb-bson-int64.html)
    
-   Десеріалізує Int64
    

# MongoDBBSONInt64::unserialize

(mongodb >=1.5.0)

MongoDBBSONInt64::unserialize — Десеріалізує Int64

### Опис

```methodsynopsis
final public MongoDB\BSON\Int64::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDB\\BSON\\Int64](class.mongodb-bson-int64.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Видає виняток [MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html)якщо властивості не можуть бути не серіалізовані (тобто `serialized` був неправильно сформований).
-   Видає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)якщо властивості неприпустимі (наприклад, відсутні поля або неприпустимі значення).

### Дивіться також

-   [MongoDB\\BSON\\Int64::serialize()](mongodb-bson-int64.serialize.html) - Серіалізує Int64
-   [unserialize()](function.unserialize.html) - Створює PHP-значення зі збереженого уявлення
-   [Сериализация объектов](language.oop5.serialization.html)