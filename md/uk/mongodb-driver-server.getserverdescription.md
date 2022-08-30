Повертає ServerDescription сервера

-   [« MongoDBDriverServer::getPort](mongodb-driver-server.getport.html)
    
-   [MongoDBDriverServer::getTags »](mongodb-driver-server.gettags.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverServer](class.mongodb-driver-server.html)
    
-   Повертає ServerDescription сервера
    

# MongoDBDriverServer::getServerDescription

(mongodb >=1.13.0)

MongoDBDriverServer::getServerDescription — Повертає ServerDescription сервера

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::getServerDescription(): MongoDB\Driver\ServerDescription
```

Повертає [MongoDBDriverServerDescription](class.mongodb-driver-serverdescription.html) сервера. Це незмінний об'єкт значення, який описуватиме сервер під час виклику методу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDBDriverServerDescription](class.mongodb-driver-serverdescription.html) сервера.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)