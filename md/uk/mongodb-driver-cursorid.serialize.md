Серіалізація CursorId

-   [« MongoDB\\Driver\\CursorId::\_\_construct](mongodb-driver-cursorid.construct.html)
    
-   [MongoDB\\Driver\\CursorId::\_\_toString »](mongodb-driver-cursorid.tostring.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\CursorId](class.mongodb-driver-cursorid.html)
    
-   Серіалізація CursorId
    

# MongoDBDriverCursorId::serialize

(mongodb >=1.7.0)

MongoDBDriverCursorId::serialize — Серіалізація CursorId

### Опис

```methodsynopsis
final public MongoDB\Driver\CursorId::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDB\\Driver\\CursorId](class.mongodb-driver-cursorid.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\CursorId::unserialize()](mongodb-driver-cursorid.unserialize.html) - Десеріалізація CursorId
-   [serialize()](function.serialize.html) - Генерує придатне для зберігання подання змінної
-   [Сериализация объектов](language.oop5.serialization.html)