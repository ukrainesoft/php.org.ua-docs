---
navigation:
  - class.mongodb-driver-monitoring-topologyopeningevent.md: « MongoDB\\Driver\\Monitoring\\TopologyOpeningEvent
  - class.mongodb-driver-monitoring-commandsubscriber.md: MongoDB\\Driver\\Monitoring\\CommandSubscriber »
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-topologyopeningevent.md: MongoDB\\Driver\\Monitoring\\TopologyOpeningEvent
title: 'MongoDB\\Driver\\Monitoring\\TopologyOpeningEvent::getTopologyId'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\TopologyOpeningEvent::getTopologyId

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\TopologyOpeningEvent::getTopologyId — Повертає ідентифікатор топології

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\TopologyOpeningEvent::getTopologyId(): MongoDB\BSON\ObjectId
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор топології.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
