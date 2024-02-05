---
navigation:
  - mongodb-driver-monitoring-commandstartedevent.getcommandname.md: '« MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getCommandName'
  - mongodb-driver-monitoring-commandstartedevent.getoperationid.md: 'MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getOperationId »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandstartedevent.md: MongoDB\\Driver\\Monitoring\\CommandStartedEvent
title: 'MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getDatabaseName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getDatabaseName

(mongodb >=1.3.0)

MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getDatabaseName — Повертає базу даних, на якій виконувалась команда

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandStartedEvent::getDatabaseName(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає базу даних, на якій було виконано команду.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
