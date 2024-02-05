---
navigation:
  - mongodb-driver-monitoring-commandfailedevent.getcommandname.md: '« MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getCommandName'
  - mongodb-driver-monitoring-commandfailedevent.geterror.md: 'MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getError »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandfailedevent.md: MongoDB\\Driver\\Monitoring\\CommandFailedEvent
title: 'MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getDurationMicros'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getDurationMicros

(mongodb >=1.3.0)

MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getDurationMicros — Повертає тривалість команди в мікросекундах

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

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
