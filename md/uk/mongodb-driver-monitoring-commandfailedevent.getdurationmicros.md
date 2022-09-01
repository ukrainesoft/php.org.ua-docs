---
navigation:
  - mongodb-driver-monitoring-commandfailedevent.getcommandname.html: '« MongoDBDriverMonitoringCommandFailedEvent::getCommandName'
  - mongodb-driver-monitoring-commandfailedevent.geterror.html: 'MongoDBDriverMonitoringCommandFailedEvent::getError »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandfailedevent.html: MongoDBDriverMonitoringCommandFailedEvent
title: 'MongoDBDriverMonitoringCommandFailedEvent::getDurationMicros'
---
# MongoDBDriverMonitoringCommandFailedEvent::getDurationMicros

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandFailedEvent::getDurationMicros — Повертає тривалість команди в мікросекундах

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandFailedEvent::getDurationMicros(): int
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
