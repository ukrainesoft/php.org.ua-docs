---
navigation:
  - mongodb-driver-monitoring-commandstartedevent.getcommand.html: '« MongoDBDriverMonitoringCommandStartedEvent::getCommand'
  - mongodb-driver-monitoring-commandstartedevent.getdatabasename.html: 'MongoDBDriverMonitoringCommandStartedEvent::getDatabaseName »'
  - index.html: PHP Manual
  - class.mongodb-driver-monitoring-commandstartedevent.html: MongoDBDriverMonitoringCommandStartedEvent
title: 'MongoDBDriverMonitoringCommandStartedEvent::getCommandName'
---
# MongoDBDriverMonitoringCommandStartedEvent::getCommandName

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandStartedEvent::getCommandName — Повертає ім'я команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandStartedEvent::getCommandName(): string
```

Повертає ім'я команди (наприклад, `"find"` `"aggregate"`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я команди.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.html)
