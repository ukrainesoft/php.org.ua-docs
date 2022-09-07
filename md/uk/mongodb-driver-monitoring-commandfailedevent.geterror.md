---
navigation:
  - mongodb-driver-monitoring-commandfailedevent.getdurationmicros.md: '« MongoDBDriverMonitoringCommandFailedEvent::getDurationMicros'
  - mongodb-driver-monitoring-commandfailedevent.getoperationid.md: 'MongoDBDriverMonitoringCommandFailedEvent::getOperationId »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandfailedevent.md: MongoDBDriverMonitoringCommandFailedEvent
title: 'MongoDBDriverMonitoringCommandFailedEvent::getError'
---
# MongoDBDriverMonitoringCommandFailedEvent::getError

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandFailedEvent::getError — Повертає виняток, пов'язаний із невдалою командою

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandFailedEvent::getError(): Exception
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає виняток ([Exception](class.exception.md)), пов'язане з невдалою командою.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
