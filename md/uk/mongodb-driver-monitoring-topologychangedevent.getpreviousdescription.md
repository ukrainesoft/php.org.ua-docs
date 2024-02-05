---
navigation:
  - mongodb-driver-monitoring-topologychangedevent.getnewdescription.md: '« MongoDB\\Driver\\Monitoring\\TopologyChangedEvent::getNewDescription'
  - mongodb-driver-monitoring-topologychangedevent.gettopologyid.md: 'MongoDB\\Driver\\Monitoring\\TopologyChangedEvent::getTopologyId »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-topologychangedevent.md: MongoDB\\Driver\\Monitoring\\TopologyChangedEvent
title: 'MongoDB\\Driver\\Monitoring\\TopologyChangedEvent::getPreviousDescription'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\TopologyChangedEvent::getPreviousDescription

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\TopologyChangedEvent::getPreviousDescription — Повертає попередній опис топології

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\TopologyChangedEvent::getPreviousDescription(): MongoDB\Driver\TopologyDescription
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає попередній опис ([MongoDB\\Driver\\TopologyDescription](class.mongodb-driver-topologydescription.md)) топології.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
