Серіалізує Regex

-   [« MongoDB\\BSON\\Regex::jsonSerialize](mongodb-bson-regex.jsonserialize.html)
    
-   [MongoDB\\BSON\\Regex::\_\_toString »](mongodb-bson-regex.tostring.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\Regex](class.mongodb-bson-regex.html)
    
-   Серіалізує Regex
    

# MongoDBBSONRegex::serialize

(mongodb >=1.2.0)

MongoDBBSONRegex::serialize — Серіалізує Regex

### Опис

```methodsynopsis
final public MongoDB\BSON\Regex::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDB\\BSON\\Regex](class.mongodb-bson-regex.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\BSON\\Regex::unserialize()](mongodb-bson-regex.unserialize.html) - десеріалізує Regex
-   [serialize()](function.serialize.html) - Генерує придатне для зберігання уявлення змінної
-   [Сериализация объектов](language.oop5.serialization.html)