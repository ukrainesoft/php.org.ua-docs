---
navigation:
  - mongodb-driver-monitoring-commandfailedevent.getserver.md: '« MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getServer'
  - mongodb-driver-monitoring-commandfailedevent.getserviceid.md: 'MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getServiceId »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandfailedevent.md: MongoDB\\Driver\\Monitoring\\CommandFailedEvent
title: 'MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getServerConnectionId'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getServerConnectionId

(mongodb >=1.14.0)

MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getServerConnectionId — Повертає ідентифікатор з'єднання з сервером для команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandFailedEvent::getServerConnectionId(): ?int
```

Повертає ідентифікатор з'єднання із сервером для команди. Ідентифікатор підключення до сервера відрізняється від сервера (тобто . [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getServer()](mongodb-driver-monitoring-commandfailedevent.getserver.md)) і повертається в поле "connectionId" відповіді команди `hello`в MongoDB 4.2+.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор з'єднання із сервером або \*\*`null`\*\*якщо він недоступний.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
