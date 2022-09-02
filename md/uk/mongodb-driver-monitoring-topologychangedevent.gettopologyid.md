---
navigation:
  - mongodb-driver-monitoring-topologychangedevent.getpreviousdescription.md: '« MongoDBDriverMonitoringTopologyChangedEvent::getPreviousDescription'
  - class.mongodb-driver-monitoring-topologyclosedevent.md: MongoDBDriverMonitoringTopologyClosedEvent »
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-topologychangedevent.md: MongoDBDriverMonitoringTopologyChangedEvent
title: 'MongoDBDriverMonitoringTopologyChangedEvent::getTopologyId'
---
# MongoDBDriverMonitoringTopologyChangedEvent::getTopologyId

(mongodb >=1.13.0)

MongoDBDriverMonitoringTopologyChangedEvent::getTopologyId — Повертає ідентифікатор топології

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\TopologyChangedEvent::getTopologyId(): MongoDB\BSON\ObjectId
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор топології.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
