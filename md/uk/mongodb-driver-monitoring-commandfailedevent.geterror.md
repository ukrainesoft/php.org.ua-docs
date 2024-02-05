---
navigation:
  - mongodb-driver-monitoring-commandfailedevent.getdurationmicros.md: '« MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getDurationMicros'
  - mongodb-driver-monitoring-commandfailedevent.getoperationid.md: 'MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getOperationId »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandfailedevent.md: MongoDB\\Driver\\Monitoring\\CommandFailedEvent
title: 'MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getError'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getError

(mongodb >=1.3.0)

MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getError — Повертає виняток, пов'язаний із невдалою командою

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandFailedEvent::getError(): Exception
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає виняток ([Exception](class.exception.md)), пов'язане з невдалою командою.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
