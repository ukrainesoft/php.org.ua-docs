---
navigation:
  - mongodb-driver-monitoring-commandstartedevent.getrequestid.md: '« MongoDBDriverMonitoringCommandStartedEvent::getRequestId'
  - mongodb-driver-monitoring-commandstartedevent.getserverconnectionid.md: 'MongoDBDriverMonitoringCommandStartedEvent::getServerConnectionId »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandstartedevent.md: MongoDBDriverMonitoringCommandStartedEvent
title: 'MongoDBDriverMonitoringCommandStartedEvent::getServer'
---
# MongoDBDriverMonitoringCommandStartedEvent::getServer

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandStartedEvent::getServer — Повертає сервер, на якому було виконано команду

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandStartedEvent::getServer(): MongoDB\Driver\Server
```

Повертає [MongoDBDriverServer](class.mongodb-driver-server.md), на якому було виконано команду.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDBDriverServer](class.mongodb-driver-server.md), на якому було виконано команду.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverMonitoringCommandFailedEvent::getServer()](mongodb-driver-monitoring-commandfailedevent.getserver.md) - Повертає сервер, на якому було виконано команду
-   [MongoDBDriverMonitoringCommandSucceededEvent::getServer()](mongodb-driver-monitoring-commandsucceededevent.getserver.md) - Повертає сервер, на якому було виконано команду
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
