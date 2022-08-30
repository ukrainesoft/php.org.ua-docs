Повертає порт, на якому прослуховується цей сервер

-   [« MongoDBDriverServerDescription::getLastUpdateTime](mongodb-driver-serverdescription.getlastupdatetime.html)
    
-   [MongoDBDriverServerDescription::getRoundTripTime »](mongodb-driver-serverdescription.getroundtriptime.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverServerDescription](class.mongodb-driver-serverdescription.html)
    
-   Повертає порт, на якому прослуховується цей сервер
    

# MongoDBDriverServerDescription::getPort

(mongodb >=1.13.0)

MongoDBDriverServerDescription::getPort — Повертає порт, на якому прослуховується цей сервер

### Опис

```methodsynopsis
final public MongoDB\Driver\ServerDescription::getPort(): int
```

Повертає порт, на якому прослуховується сервер.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає порт, на якому прослуховується сервер.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverServer::getPort()](mongodb-driver-server.getport.html) - Повертає порт, який слухає сервер