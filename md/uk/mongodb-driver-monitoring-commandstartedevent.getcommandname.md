---
navigation:
  - mongodb-driver-monitoring-commandstartedevent.getcommand.md: '« MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getCommand'
  - mongodb-driver-monitoring-commandstartedevent.getdatabasename.md: 'MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getDatabaseName »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandstartedevent.md: MongoDB\\Driver\\Monitoring\\CommandStartedEvent
title: 'MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getCommandName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getCommandName

(mongodb >=1.3.0)

MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getCommandName — Повертає ім'я команди

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

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
