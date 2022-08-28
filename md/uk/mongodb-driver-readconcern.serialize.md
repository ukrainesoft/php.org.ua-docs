Серіалізація ReadConcern

-   [« MongoDB\\Driver\\ReadConcern::isDefault](mongodb-driver-readconcern.isdefault.html)
    
-   [MongoDB\\Driver\\ReadConcern::unserialize »](mongodb-driver-readconcern.unserialize.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\ReadConcern](class.mongodb-driver-readconcern.html)
    
-   Серіалізація ReadConcern
    

# MongoDBDriverReadConcern::serialize

(mongodb >=1.7.0)

MongoDBDriverReadConcern::serialize — Серіалізація ReadConcern

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadConcern::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDB\\Driver\\ReadConcern](class.mongodb-driver-readconcern.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\ReadConcern::unserialize()](mongodb-driver-readconcern.unserialize.html) - Десеріалізація ReadConcern
-   [serialize()](function.serialize.html) - Генерує придатне для зберігання подання змінної
-   [Сериализация объектов](language.oop5.serialization.html)