---
navigation:
  - class.mongodb-driver-monitoring-topologychangedevent.md: « MongoDB\\Driver\\Monitoring\\TopologyChangedEvent
  - mongodb-driver-monitoring-topologychangedevent.getpreviousdescription.md: >-
      MongoDB\\Driver\\Monitoring\\TopologyChangedEvent::getPreviousDescription
      »
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-topologychangedevent.md: MongoDB\\Driver\\Monitoring\\TopologyChangedEvent
title: 'MongoDB\\Driver\\Monitoring\\TopologyChangedEvent::getNewDescription'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\TopologyChangedEvent::getNewDescription

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\TopologyChangedEvent::getNewDescription — Повертає новий опис топології

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\TopologyChangedEvent::getNewDescription(): MongoDB\Driver\TopologyDescription
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає новий опис ([MongoDB\\Driver\\TopologyDescription](class.mongodb-driver-topologydescription.md)) топології.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
