---
navigation:
  - mongodb-driver-monitoring-commandsucceededevent.getrequestid.md: '« MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getRequestId'
  - mongodb-driver-monitoring-commandsucceededevent.getserverconnectionid.md: >-
      MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getServerConnectionId
      »
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandsucceededevent.md: MongoDB\\Driver\\Monitoring\\CommandSucceededEvent
title: 'MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getServer'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getServer

(mongodb >=1.3.0)

MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getServer — Повертає сервер, на якому було виконано команду

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandSucceededEvent::getServer(): MongoDB\Driver\Server
```

Повертає [MongoDB\\Driver\\Server](class.mongodb-driver-server.md), на якому було виконано команду.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDB\\Driver\\Server](class.mongodb-driver-server.md), на якому було виконано команду.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getServer()](mongodb-driver-monitoring-commandstartedevent.getserver.md) \- Повертає сервер, на якому було виконано команду
-   [MongoDB\\Driver\\Cursor::getServer()](mongodb-driver-cursor.getserver.md) \- Повертає сервер, пов'язаний із курсором
-   [MongoDB\\Driver\\WriteResult::getServer()](mongodb-driver-writeresult.getserver.md) \- Повертає сервер, пов'язаний із цим результатом запису
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
