---
navigation:
  - class.mongodb-driver-monitoring-commandsucceededevent.md: « MongoDB\\Driver\\Monitoring\\CommandSucceededEvent
  - mongodb-driver-monitoring-commandsucceededevent.getdurationmicros.md: 'MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getDurationMicros »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandsucceededevent.md: MongoDB\\Driver\\Monitoring\\CommandSucceededEvent
title: 'MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getCommandName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getCommandName

(mongodb >=1.3.0)

MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getCommandName — Повертає ім'я команди

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

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
