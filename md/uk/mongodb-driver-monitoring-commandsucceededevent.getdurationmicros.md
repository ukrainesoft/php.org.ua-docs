---
navigation:
  - mongodb-driver-monitoring-commandsucceededevent.getcommandname.md: '« MongoDBDriverMonitoringCommandSucceededEvent::getCommandName'
  - mongodb-driver-monitoring-commandsucceededevent.getoperationid.md: 'MongoDBDriverMonitoringCommandSucceededEvent::getOperationId »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandsucceededevent.md: MongoDBDriverMonitoringCommandSucceededEvent
title: 'MongoDBDriverMonitoringCommandSucceededEvent::getDurationMicros'
---
# MongoDBDriverMonitoringCommandSucceededEvent::getDurationMicros

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandSucceededEvent::getDurationMicros — Повертає тривалість команди в мікросекундах

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandSucceededEvent::getDurationMicros(): int
```

Тривалість команди - це розраховане значення, яке включає час надсилання повідомлення та отримання відповіді від сервера.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає тривалість команди у мікросекундах.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
