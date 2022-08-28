Серіалізація ReadPreference

-   [« MongoDB\\Driver\\ReadPreference::getTagSets](mongodb-driver-readpreference.gettagsets.html)
    
-   [MongoDB\\Driver\\ReadPreference::unserialize »](mongodb-driver-readpreference.unserialize.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\ReadPreference](class.mongodb-driver-readpreference.html)
    
-   Серіалізація ReadPreference
    

# MongoDBDriverReadPreference::serialize

(mongodb >=1.7.0)

MongoDBDriverReadPreference::serialize — Серіалізація ReadPreference

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadPreference::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDB\\Driver\\ReadPreference](class.mongodb-driver-readpreference.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\ReadPreference::unserialize()](mongodb-driver-readpreference.unserialize.html) - Десеріалізація ReadPreference
-   [serialize()](function.serialize.html) - Генерує придатне для зберігання подання змінної
-   [Сериализация объектов](language.oop5.serialization.html)