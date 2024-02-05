---
navigation:
  - mongodb-driver-monitoring-serveropeningevent.gethost.md: '« MongoDB\\Driver\\Monitoring\\ServerOpeningEvent::getHost'
  - mongodb-driver-monitoring-serveropeningevent.gettopologyid.md: 'MongoDB\\Driver\\Monitoring\\ServerOpeningEvent::getTopologyId »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serveropeningevent.md: MongoDB\\Driver\\Monitoring\\ServerOpeningEvent
title: 'MongoDB\\Driver\\Monitoring\\ServerOpeningEvent::getPort'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\ServerOpeningEvent::getPort

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\ServerOpeningEvent::getPort — Повертає порт, на якому прослуховується сервер

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerOpeningEvent::getPort(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає порт, у якому прослуховується сервер.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
