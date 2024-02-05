---
navigation:
  - mongodb-driver-monitoring-topologychangedevent.getpreviousdescription.md: >-
      «
      MongoDB\\Driver\\Monitoring\\TopologyChangedEvent::getPreviousDescription
  - class.mongodb-driver-monitoring-topologyclosedevent.md: MongoDB\\Driver\\Monitoring\\TopologyClosedEvent »
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-topologychangedevent.md: MongoDB\\Driver\\Monitoring\\TopologyChangedEvent
title: 'MongoDB\\Driver\\Monitoring\\TopologyChangedEvent::getTopologyId'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\TopologyChangedEvent::getTopologyId

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\TopologyChangedEvent::getTopologyId — Повертає ідентифікатор топології

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\TopologyChangedEvent::getTopologyId(): MongoDB\BSON\ObjectId
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор топології.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
