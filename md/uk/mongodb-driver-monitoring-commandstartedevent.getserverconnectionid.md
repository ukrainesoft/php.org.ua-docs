---
navigation:
  - mongodb-driver-monitoring-commandstartedevent.getserver.md: '« MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getServer'
  - mongodb-driver-monitoring-commandstartedevent.getserviceid.md: 'MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getServiceId »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandstartedevent.md: MongoDB\\Driver\\Monitoring\\CommandStartedEvent
title: 'MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getServerConnectionId'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getServerConnectionId

(mongodb >=1.14.0)

MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getServerConnectionId — Повертає ідентифікатор з'єднання із сервером для команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandStartedEvent::getServerConnectionId(): ?int
```

Повертає ідентифікатор з'єднання із сервером для команди. Ідентифікатор з'єднання з сервером відрізняється від сервера (тобто . [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getServer()](mongodb-driver-monitoring-commandstartedevent.getserver.md)) і повертається у поле "connectionId" з відповіді команди `hello`в MongoDB 4.2+.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор з'єднання із сервером або \*\*`null`\*\*якщо він недоступний.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
