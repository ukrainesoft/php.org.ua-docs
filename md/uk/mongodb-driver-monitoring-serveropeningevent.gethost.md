---
navigation:
  - class.mongodb-driver-monitoring-serveropeningevent.md: « MongoDB\\Driver\\Monitoring\\ServerOpeningEvent
  - mongodb-driver-monitoring-serveropeningevent.getport.md: 'MongoDB\\Driver\\Monitoring\\ServerOpeningEvent::getPort »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serveropeningevent.md: MongoDB\\Driver\\Monitoring\\ServerOpeningEvent
title: 'MongoDB\\Driver\\Monitoring\\ServerOpeningEvent::getHost'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\ServerOpeningEvent::getHost

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\ServerOpeningEvent::getHost — Повертає ім'я сервера.

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerOpeningEvent::getHost(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я сервера хоста.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
