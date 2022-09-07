---
navigation:
  - mongodb-driver-monitoring-topologychangedevent.getnewdescription.md: '« MongoDBDriverMonitoringTopologyChangedEvent::getNewDescription'
  - mongodb-driver-monitoring-topologychangedevent.gettopologyid.md: 'MongoDBDriverMonitoringTopologyChangedEvent::getTopologyId »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-topologychangedevent.md: MongoDBDriverMonitoringTopologyChangedEvent
title: 'MongoDBDriverMonitoringTopology Changed Event::get Previous Description'
---
# MongoDBDriverMonitoringTopology Changed Event::get Previous Description

(mongodb >=1.13.0)

MongoDBDriverMonitoringTopologyChangedEvent::getPreviousDescription — Повертає попередній опис топології

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\TopologyChangedEvent::getPreviousDescription(): MongoDB\Driver\TopologyDescription
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає попередній опис ([MongoDBDriverTopologyDescription](class.mongodb-driver-topologydescription.md)) топології.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
