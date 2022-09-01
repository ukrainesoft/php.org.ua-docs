---
navigation:
  - class.mongodb-driver-monitoring-commandsucceededevent.html: « MongoDBDriverMonitoringCommandSucceededEvent
  - mongodb-driver-monitoring-commandsucceededevent.getdurationmicros.html: 'MongoDBDriverMonitoringCommandSucceededEvent::getDurationMicros »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandsucceededevent.html: MongoDBDriverMonitoringCommandSucceededEvent
title: 'MongoDBDriverMonitoringCommandSucceededEvent::getCommandName'
---
# MongoDBDriverMonitoringCommandSucceededEvent::getCommandName

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandSucceededEvent::getCommandName — Повертає ім'я команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandSucceededEvent::getCommandName(): string
```

Повертає ім'я команди (наприклад, `"find"` `"aggregate"`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я команди.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
