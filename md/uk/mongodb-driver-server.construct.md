Створює новий Server (не використовується)

-   [« MongoDBDriverServer](class.mongodb-driver-server.html)
    
-   [MongoDBDriverServer::executeBulkWrite »](mongodb-driver-server.executebulkwrite.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverServer](class.mongodb-driver-server.html)
    
-   Створює новий Server (не використовується)
    

# MongoDBDriverServer::construct

(mongodb >=1.0.0)

MongoDBDriverServer::construct — Створює новий сервер (не використовується)

### Опис

```methodsynopsis
final private MongoDB\Driver\Server::__construct()
```

Об'єкти [MongoDBDriverServer](class.mongodb-driver-server.html) створюються всередині [MongoDBDriverManager](class.mongodb-driver-manager.html), коли з'єднання з базою даних встановлено і можуть бути повернуті [MongoDBDriverManager::getServers()](mongodb-driver-manager.getservers.html) і [MongoDBDriverManager::selectServer()](mongodb-driver-manager.selectserver.html)

### Список параметрів

Ця функція не має параметрів.

### Дивіться також

-   [MongoDBDriverManager::getServers()](mongodb-driver-manager.getservers.html) - Повертає сервери, до яких підключено менеджера
-   [MongoDBDriverManager::selectServer()](mongodb-driver-manager.selectserver.html) - Вибрати сервер, що відповідає перевагам читання