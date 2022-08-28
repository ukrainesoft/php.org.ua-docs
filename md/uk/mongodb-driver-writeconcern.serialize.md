Серіалізація WriteConcern

-   [« MongoDB\\Driver\\WriteConcern::isDefault](mongodb-driver-writeconcern.isdefault.html)
    
-   [MongoDB\\Driver\\WriteConcern::unserialize »](mongodb-driver-writeconcern.unserialize.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\WriteConcern](class.mongodb-driver-writeconcern.html)
    
-   Серіалізація WriteConcern
    

# MongoDBDriverWriteConcern::serialize

(mongodb >=1.7.0)

MongoDBDriverWriteConcern::serialize — Серіалізація WriteConcern

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteConcern::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDB\\Driver\\WriteConcern](class.mongodb-driver-writeconcern.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\WriteConcern::unserialize()](mongodb-driver-writeconcern.unserialize.html) - Десеріалізація WriteConcern
-   [serialize()](function.serialize.html) - Генерує придатне для зберігання подання змінної
-   [Сериализация объектов](language.oop5.serialization.html)