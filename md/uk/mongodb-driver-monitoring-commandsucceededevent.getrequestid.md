---
navigation:
  - mongodb-driver-monitoring-commandsucceededevent.getreply.md: '« MongoDBDriverMonitoringCommandSucceededEvent::getReply'
  - mongodb-driver-monitoring-commandsucceededevent.getserver.md: 'MongoDBDriverMonitoringCommandSucceededEvent::getServer »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandsucceededevent.md: MongoDBDriverMonitoringCommandSucceededEvent
title: 'MongoDBDriverMonitoringCommandSucceededEvent::getRequestId'
---
# MongoDBDriverMonitoringCommandSucceededEvent::getRequestId

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandSucceededEvent::getRequestId — Повертає ідентифікатор запиту команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandSucceededEvent::getRequestId(): string
```

Ідентифікатор запиту генерується драйвером і може бути використаний для зв'язування [MongoDBDriverMonitoringCommandSucceededEvent](class.mongodb-driver-monitoring-commandsucceededevent.md) з попереднім [MongoDBDriverMonitoringCommandStartedEvent](class.mongodb-driver-monitoring-commandstartedevent.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор запиту команди.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverMonitoringCommandStartedEvent::getRequestId()](mongodb-driver-monitoring-commandstartedevent.getrequestid.md) - Повертає ідентифікатор запиту команди
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
