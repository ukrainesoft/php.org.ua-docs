Повертає ціле число, що означає тип цього сервера

-   [« MongoDB\\Driver\\Server::getTags](mongodb-driver-server.gettags.html)
    
-   [MongoDB\\Driver\\Server::isArbiter »](mongodb-driver-server.isarbiter.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Server](class.mongodb-driver-server.html)
    
-   Повертає ціле число, що означає тип цього сервера
    

# MongoDBDriverServer::getType

(mongodb >=1.0.0)

MongoDBDriverServer::getType — Повертає ціле число, яке означає тип цього сервера

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::getType(): int
```

Повертає int, що означає тип цього сервера. Значення буде відповідати константі [MongoDB\\Driver\\Server](class.mongodb-driver-server.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає int, що означає тип цього сервера.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Server::getInfo()](mongodb-driver-server.getinfo.html) - Повертає масив інформації, що описує сервер
-   [MongoDB\\Driver\\ServerDescription::getType()](mongodb-driver-serverdescription.gettype.html) - Повертає рядок, що позначає тип сервера