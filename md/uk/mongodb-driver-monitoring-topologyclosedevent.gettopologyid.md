---
navigation:
  - class.mongodb-driver-monitoring-topologyclosedevent.md: « MongoDB\\Driver\\Monitoring\\TopologyClosedEvent
  - class.mongodb-driver-monitoring-topologyopeningevent.md: MongoDB\\Driver\\Monitoring\\TopologyOpeningEvent »
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-topologyclosedevent.md: MongoDB\\Driver\\Monitoring\\TopologyClosedEvent
title: 'MongoDB\\Driver\\Monitoring\\TopologyClosedEvent::getTopologyId'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\TopologyClosedEvent::getTopologyId

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\TopologyClosedEvent::getTopologyId — Повертає ідентифікатор топології

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\TopologyClosedEvent::getTopologyId(): MongoDB\BSON\ObjectId
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор топології.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
