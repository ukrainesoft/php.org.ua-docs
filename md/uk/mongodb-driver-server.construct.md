Створює новий Server (не використовується)

-   [« MongoDB\\Driver\\Server](class.mongodb-driver-server.html)
    
-   [MongoDB\\Driver\\Server::executeBulkWrite »](mongodb-driver-server.executebulkwrite.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Server](class.mongodb-driver-server.html)
    
-   Створює новий Server (не використовується)
    

# MongoDBDriverServer::construct

(mongodb >=1.0.0)

MongoDBDriverServer::construct — Створює новий сервер (не використовується)

### Опис

```methodsynopsis
final private MongoDB\Driver\Server::__construct()
```

Об'єкти [MongoDB\\Driver\\Server](class.mongodb-driver-server.html) створюються всередині [MongoDB\\Driver\\Manager](class.mongodb-driver-manager.html), коли з'єднання з базою даних встановлено і можуть бути повернуті [MongoDB\\Driver\\Manager::getServers()](mongodb-driver-manager.getservers.html) і [MongoDB\\Driver\\Manager::selectServer()](mongodb-driver-manager.selectserver.html)

### Список параметрів

Ця функція не має параметрів.

### Дивіться також

-   [MongoDB\\Driver\\Manager::getServers()](mongodb-driver-manager.getservers.html) - Повертає сервери, до яких підключено менеджера
-   [MongoDB\\Driver\\Manager::selectServer()](mongodb-driver-manager.selectserver.html) - Вибрати сервер, що відповідає перевагам читання