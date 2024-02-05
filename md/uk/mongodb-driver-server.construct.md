---
navigation:
  - class.mongodb-driver-server.md: « MongoDB\\Driver\\Server
  - mongodb-driver-server.executebulkwrite.md: 'MongoDB\\Driver\\Server::executeBulkWrite »'
  - index.md: PHP Manual
  - class.mongodb-driver-server.md: MongoDB\\Driver\\Server
title: 'MongoDB\\Driver\\Server::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Server::\_\_construct

(mongodb >=1.0.0)

MongoDB\\Driver\\Server::\_\_construct — Створює новий сервер (не використовується)

### Опис

```methodsynopsis
final private MongoDB\Driver\Server::__construct()
```

Об'єкти [MongoDB\\Driver\\Server](class.mongodb-driver-server.md) створюються всередині [MongoDB\\Driver\\Manager](class.mongodb-driver-manager.md), коли з'єднання з базою даних встановлено і можуть бути повернуті [MongoDB\\Driver\\Manager::getServers()](mongodb-driver-manager.getservers.md) і [MongoDB\\Driver\\Manager::selectServer()](mongodb-driver-manager.selectserver.md)

### Список параметрів

Ця функція не має параметрів.

### Дивіться також

-   [MongoDB\\Driver\\Manager::getServers()](mongodb-driver-manager.getservers.md) \- Повертає сервери, до яких підключено менеджера
-   [MongoDB\\Driver\\Manager::selectServer()](mongodb-driver-manager.selectserver.md) \- Вибрати сервер, що відповідає перевагам читання
