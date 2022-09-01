---
navigation:
  - mongodb-driver-monitoring-commandfailedevent.getserver.html: '« MongoDBDriverMonitoringCommandFailedEvent::getServer'
  - mongodb-driver-monitoring-commandfailedevent.getserviceid.html: 'MongoDBDriverMonitoringCommandFailedEvent::getServiceId »'
  - index.html: PHP Manual
  - class.mongodb-driver-monitoring-commandfailedevent.html: MongoDBDriverMonitoringCommandFailedEvent
title: 'MongoDBDriverMonitoringCommandFailedEvent::getServerConnectionId'
---
# MongoDBDriverMonitoringCommandFailedEvent::getServerConnectionId

(mongodb >=1.14.0)

MongoDBDriverMonitoringCommandFailedEvent::getServerConnectionId — Повертає ідентифікатор з'єднання з сервером для команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandFailedEvent::getServerConnectionId(): ?int
```

Повертає ідентифікатор з'єднання із сервером для команди. Ідентифікатор підключення до сервера відрізняється від сервера (тобто . [MongoDBDriverMonitoringCommandFailedEvent::getServer()](mongodb-driver-monitoring-commandfailedevent.getserver.html)) і повертається в поле "connectionId" відповіді команди `hello` у MongoDB 4.2+.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор з'єднання із сервером або \*\*`null`\*\*якщо він недоступний.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
