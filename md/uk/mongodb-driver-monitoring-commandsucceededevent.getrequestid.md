---
navigation:
  - mongodb-driver-monitoring-commandsucceededevent.getreply.md: '« MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getReply'
  - mongodb-driver-monitoring-commandsucceededevent.getserver.md: 'MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getServer »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandsucceededevent.md: MongoDB\\Driver\\Monitoring\\CommandSucceededEvent
title: 'MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getRequestId'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getRequestId

(mongodb >=1.3.0)

MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getRequestId — Повертає ідентифікатор запиту команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandSucceededEvent::getRequestId(): string
```

Ідентифікатор запиту генерується драйвером і може бути використаний для зв'язування [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent](class.mongodb-driver-monitoring-commandsucceededevent.md) з попереднім [MongoDB\\Driver\\Monitoring\\CommandStartedEvent](class.mongodb-driver-monitoring-commandstartedevent.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор запиту команди.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getRequestId()](mongodb-driver-monitoring-commandstartedevent.getrequestid.md) \- Повертає ідентифікатор запиту команди
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
