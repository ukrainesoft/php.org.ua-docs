---
navigation:
  - mongodb-driver-monitoring-serverclosedevent.getport.md: '« MongoDB\\Driver\\Monitoring\\ServerClosedEvent::getPort'
  - class.mongodb-driver-monitoring-serveropeningevent.md: MongoDB\\Driver\\Monitoring\\ServerOpeningEvent »
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverclosedevent.md: MongoDB\\Driver\\Monitoring\\ServerClosedEvent
title: 'MongoDB\\Driver\\Monitoring\\ServerClosedEvent::getTopologyId'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\ServerClosedEvent::getTopologyId

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\ServerClosedEvent::getTopologyId — Повертає ідентифікатор топології, пов'язаний із цим сервером

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerClosedEvent::getTopologyId(): MongoDB\BSON\ObjectId
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор топології.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
