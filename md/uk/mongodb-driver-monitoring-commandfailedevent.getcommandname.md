---
navigation:
  - class.mongodb-driver-monitoring-commandfailedevent.md: « MongoDB\\Driver\\Monitoring\\CommandFailedEvent
  - mongodb-driver-monitoring-commandfailedevent.getdurationmicros.md: 'MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getDurationMicros »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandfailedevent.md: MongoDB\\Driver\\Monitoring\\CommandFailedEvent
title: 'MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getCommandName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getCommandName

(mongodb >=1.3.0)

MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getCommandName — Повертає ім'я команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandFailedEvent::getCommandName(): string
```

Повертає ім'я команди (наприклад, `"find"` `"aggregate"`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я команди.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
