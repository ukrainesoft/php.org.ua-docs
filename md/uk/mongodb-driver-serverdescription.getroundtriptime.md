Повертає час обходу сервера у мілісекундах

-   [« MongoDBDriverServerDescription::getPort](mongodb-driver-serverdescription.getport.html)
    
-   [MongoDBDriverServerDescription::getType »](mongodb-driver-serverdescription.gettype.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverServerDescription](class.mongodb-driver-serverdescription.html)
    
-   Повертає час обходу сервера у мілісекундах
    

# MongoDBDriverServerDescription::getRoundTripTime

(mongodb >=1.13.0)

MongoDBDriverServerDescription::getRoundTripTime — Повертає час обходу сервера в мілісекундах

### Опис

```methodsynopsis
final public MongoDB\Driver\ServerDescription::getRoundTripTime(): ?int
```

Повертає час обходу сервера у мілісекундах. Це вимір тривалості команди [» hello](https://www.mongodb.com/docs/manual/reference/command/hello/)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає час обходу сервера у мілісекундах.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverServer::getLatency()](mongodb-driver-server.getlatency.html) - Повертає затримку сервера у мілісекундах