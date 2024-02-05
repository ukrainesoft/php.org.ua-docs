---
navigation:
  - mongodb-driver-monitoring-commandsucceededevent.getserver.md: '« MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getServer'
  - mongodb-driver-monitoring-commandsucceededevent.getserviceid.md: 'MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getServiceId »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandsucceededevent.md: MongoDB\\Driver\\Monitoring\\CommandSucceededEvent
title: 'MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getServerConnectionId'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getServerConnectionId

(mongodb >=1.14.0)

MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getServerConnectionId — Повертає ідентифікатор з'єднання з сервером для команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandSucceededEvent::getServerConnectionId(): ?int
```

Повертає ідентифікатор з'єднання із сервером для команди. Ідентифікатор з'єднання з сервером відрізняється від сервера (тобто . [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getServer()](mongodb-driver-monitoring-commandsucceededevent.getserver.md)) і повертається у поле "connectionId" з відповіді команди `hello`в MongoDB 4.2+.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор з'єднання із сервером або \*\*`null`\*\*якщо він недоступний.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
