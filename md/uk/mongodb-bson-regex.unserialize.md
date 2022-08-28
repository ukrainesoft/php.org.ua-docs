Десеріалізує Regex

-   [« MongoDB\\BSON\\Regex::\_\_toString](mongodb-bson-regex.tostring.html)
    
-   [MongoDB\\BSON\\Timestamp »](class.mongodb-bson-timestamp.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\Regex](class.mongodb-bson-regex.html)
    
-   Десеріалізує Regex
    

# MongoDBBSONRegex::unserialize

(mongodb >=1.2.0)

MongoDBBSONRegex::unserialize — Десеріалізує Regex

### Опис

```methodsynopsis
final public MongoDB\BSON\Regex::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDB\\BSON\\Regex](class.mongodb-bson-regex.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Видає [MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html)якщо властивості не можуть бути не серіалізовані (наприклад, `serialized` був неправильно сформований).
-   Видає [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)якщо властивості неприпустимі (наприклад, відсутні поля або неприпустимі значення).

### Дивіться також

-   [MongoDB\\BSON\\Regex::serialize()](mongodb-bson-regex.serialize.html) - Серіалізує Regex
-   [unserialize()](function.unserialize.html) - Створює PHP-значення зі збереженого уявлення
-   [Сериализация объектов](language.oop5.serialization.html)