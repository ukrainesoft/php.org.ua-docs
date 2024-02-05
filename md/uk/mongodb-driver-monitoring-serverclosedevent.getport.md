---
navigation:
  - mongodb-driver-monitoring-serverclosedevent.gethost.md: '« MongoDB\\Driver\\Monitoring\\ServerClosedEvent::getHost'
  - mongodb-driver-monitoring-serverclosedevent.gettopologyid.md: 'MongoDB\\Driver\\Monitoring\\ServerClosedEvent::getTopologyId »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverclosedevent.md: MongoDB\\Driver\\Monitoring\\ServerClosedEvent
title: 'MongoDB\\Driver\\Monitoring\\ServerClosedEvent::getPort'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\ServerClosedEvent::getPort

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\ServerClosedEvent::getPort — Повертає порт, на якому прослуховується сервер

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerClosedEvent::getPort(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає порт, у якому прослуховується сервер.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
