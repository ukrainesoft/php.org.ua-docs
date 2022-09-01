---
navigation:
  - mongodb-driver-monitoring-commandfailedevent.getrequestid.html: '« MongoDBDriverMonitoringCommandFailedEvent::getRequestId'
  - mongodb-driver-monitoring-commandfailedevent.getserverconnectionid.html: 'MongoDBDriverMonitoringCommandFailedEvent::getServerConnectionId »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandfailedevent.html: MongoDBDriverMonitoringCommandFailedEvent
title: 'MongoDBDriverMonitoringCommandFailedEvent::getServer'
---
# MongoDBDriverMonitoringCommandFailedEvent::getServer

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandFailedEvent::getServer — Повертає сервер, на якому було виконано команду

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandFailedEvent::getServer(): MongoDB\Driver\Server
```

Повертає [MongoDBDriverServer](class.mongodb-driver-server.md), на якому було виконано команду.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDBDriverServer](class.mongodb-driver-server.md), на якому було виконано команду.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverMonitoringCommandStartedEvent::getServer()](mongodb-driver-monitoring-commandstartedevent.getserver.md) - Повертає сервер, на якому було виконано команду
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
