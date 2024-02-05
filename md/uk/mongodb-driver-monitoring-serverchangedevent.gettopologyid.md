---
navigation:
  - mongodb-driver-monitoring-serverchangedevent.getpreviousdescription.md: '« MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getPreviousDescription'
  - class.mongodb-driver-monitoring-serverclosedevent.md: MongoDB\\Driver\\Monitoring\\ServerClosedEvent »
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverchangedevent.md: MongoDB\\Driver\\Monitoring\\ServerChangedEvent
title: 'MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getTopologyId'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getTopologyId

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getTopologyId — Повертає ідентифікатор топології, пов'язаний із цим сервером

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerChangedEvent::getTopologyId(): MongoDB\BSON\ObjectId
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор топології.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
