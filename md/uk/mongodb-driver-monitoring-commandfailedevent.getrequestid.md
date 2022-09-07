---
navigation:
  - mongodb-driver-monitoring-commandfailedevent.getreply.md: '« MongoDBDriverMonitoringCommandFailedEvent::getReply'
  - mongodb-driver-monitoring-commandfailedevent.getserver.md: 'MongoDBDriverMonitoringCommandFailedEvent::getServer »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandfailedevent.md: MongoDBDriverMonitoringCommandFailedEvent
title: 'MongoDBDriverMonitoringCommandFailedEvent::getRequestId'
---
# MongoDBDriverMonitoringCommandFailedEvent::getRequestId

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandFailedEvent::getRequestId — Повертає ідентифікатор запиту команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandFailedEvent::getRequestId(): string
```

Ідентифікатор запиту генерується драйвером і може бути використаний для зв'язування [MongoDBDriverMonitoringCommandFailedEvent](class.mongodb-driver-monitoring-commandfailedevent.md) з попереднім [MongoDBDriverMonitoringCommandStartedEvent](class.mongodb-driver-monitoring-commandstartedevent.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор запиту команди.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverMonitoringCommandStartedEvent::getRequestId()](mongodb-driver-monitoring-commandstartedevent.getrequestid.md) - Повертає ідентифікатор запиту команди
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
