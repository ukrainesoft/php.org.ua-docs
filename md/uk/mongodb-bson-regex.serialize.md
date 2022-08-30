Серіалізує Regex

-   [« MongoDBBSONRegex::jsonSerialize](mongodb-bson-regex.jsonserialize.html)
    
-   [MongoDBBSONRegex::toString »](mongodb-bson-regex.tostring.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBBSONRegex](class.mongodb-bson-regex.html)
    
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

Повертає серіалізовану виставу [MongoDBBSONRegex](class.mongodb-bson-regex.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBBSONRegex::unserialize()](mongodb-bson-regex.unserialize.html) - десеріалізує Regex
-   [serialize()](function.serialize.html) - Генерує придатне для зберігання уявлення змінної
-   [Серіалізація об'єктів](language.oop5.serialization.html)