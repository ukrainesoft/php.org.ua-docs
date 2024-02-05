---
navigation:
  - mongodb-driver-monitoring-commandfailedevent.getreply.md: '« MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getReply'
  - mongodb-driver-monitoring-commandfailedevent.getserver.md: 'MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getServer »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandfailedevent.md: MongoDB\\Driver\\Monitoring\\CommandFailedEvent
title: 'MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getRequestId'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getRequestId

(mongodb >=1.3.0)

MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getRequestId — Повертає ідентифікатор запиту команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandFailedEvent::getRequestId(): string
```

Ідентифікатор запиту генерується драйвером і може бути використаний для зв'язування [MongoDB\\Driver\\Monitoring\\CommandFailedEvent](class.mongodb-driver-monitoring-commandfailedevent.md) з попереднім [MongoDB\\Driver\\Monitoring\\CommandStartedEvent](class.mongodb-driver-monitoring-commandstartedevent.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор запиту команди.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getRequestId()](mongodb-driver-monitoring-commandstartedevent.getrequestid.md) \- Повертає ідентифікатор запиту команди
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
