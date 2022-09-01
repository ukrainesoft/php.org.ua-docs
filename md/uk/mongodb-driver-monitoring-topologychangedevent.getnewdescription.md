---
navigation:
  - class.mongodb-driver-monitoring-topologychangedevent.html: « MongoDBDriverMonitoringTopologyChangedEvent
  - mongodb-driver-monitoring-topologychangedevent.getpreviousdescription.html: 'MongoDBDriverMonitoringTopologyChangedEvent::getPreviousDescription »'
  - index.html: PHP Manual
  - class.mongodb-driver-monitoring-topologychangedevent.html: MongoDBDriverMonitoringTopologyChangedEvent
title: 'MongoDBDriverMonitoringTopologyChangedEvent::getNewDescription'
---
# MongoDBDriverMonitoringTopologyChangedEvent::getNewDescription

(mongodb >=1.13.0)

MongoDBDriverMonitoringTopologyChangedEvent::getNewDescription — Повертає новий опис топології

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\TopologyChangedEvent::getNewDescription(): MongoDB\Driver\TopologyDescription
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає новий опис ([MongoDBDriverTopologyDescription](class.mongodb-driver-topologydescription.html)) топології.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
