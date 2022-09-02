---
navigation:
  - class.mongodb-driver-server.md: « MongoDBDriverServer
  - mongodb-driver-server.executebulkwrite.md: 'MongoDBDriverServer::executeBulkWrite »'
  - index.md: PHP Manual
  - class.mongodb-driver-server.md: MongoDBDriverServer
title: 'MongoDBDriverServer::construct'
---
# MongoDBDriverServer::construct

(mongodb >=1.0.0)

MongoDBDriverServer::construct — Створює новий сервер (не використовується)

### Опис

```methodsynopsis
final private MongoDB\Driver\Server::__construct()
```

Об'єкти [MongoDBDriverServer](class.mongodb-driver-server.md) створюються всередині [MongoDBDriverManager](class.mongodb-driver-manager.md), коли з'єднання з базою даних встановлено і можуть бути повернуті [MongoDBDriverManager::getServers()](mongodb-driver-manager.getservers.md) і [MongoDBDriverManager::selectServer()](mongodb-driver-manager.selectserver.md)

### Список параметрів

Ця функція не має параметрів.

### Дивіться також

-   [MongoDBDriverManager::getServers()](mongodb-driver-manager.getservers.md) - Повертає сервери, до яких підключено менеджера
-   [MongoDBDriverManager::selectServer()](mongodb-driver-manager.selectserver.md) - Вибрати сервер, що відповідає перевагам читання
