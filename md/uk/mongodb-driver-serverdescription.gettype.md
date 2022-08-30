Повертає рядок, який позначає тип сервера

-   [« MongoDBDriverServerDescription::getRoundTripTime](mongodb-driver-serverdescription.getroundtriptime.html)
    
-   [MongoDBDriverTopologyDescription »](class.mongodb-driver-topologydescription.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverServerDescription](class.mongodb-driver-serverdescription.html)
    
-   Повертає рядок, який позначає тип сервера
    

# MongoDBDriverServerDescription::getType

(mongodb >=1.13.0)

MongoDBDriverServerDescription::getType — Повертає рядок, який позначає тип сервера

### Опис

```methodsynopsis
final public MongoDB\Driver\ServerDescription::getType(): string
```

Повертає рядок (string), що позначає тип сервера. Значення співвідноситиметься з константою [MongoDBDriverServerDescription](class.mongodb-driver-serverdescription.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок (string), що позначає тип сервера.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverServer::getType()](mongodb-driver-server.gettype.html) - Повертає ціле число, що означає тип цього сервера