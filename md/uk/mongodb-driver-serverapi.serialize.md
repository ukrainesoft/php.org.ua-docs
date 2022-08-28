Серіалізує ServerApi

-   [« MongoDB\\Driver\\ServerApi::\_\_construct](mongodb-driver-serverapi.construct.html)
    
-   [MongoDB\\Driver\\ServerApi::unserialize »](mongodb-driver-serverapi.unserialize.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\ServerApi](class.mongodb-driver-serverapi.html)
    
-   Серіалізує ServerApi
    

# MongoDBDriverServerApi::serialize

(mongodb >=1.10.0)

MongoDBDriverServerApi::serialize — Серіалізує ServerApi

### Опис

```methodsynopsis
final public MongoDB\Driver\ServerApi::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDB\\Driver\\ServerApi](class.mongodb-driver-serverapi.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\ServerApi::unserialize()](mongodb-driver-serverapi.unserialize.html) - Десеріалізує ServerApi
-   [serialize()](function.serialize.html) - Генерує придатне для зберігання уявлення змінної
-   [Сериализация объектов](language.oop5.serialization.html)