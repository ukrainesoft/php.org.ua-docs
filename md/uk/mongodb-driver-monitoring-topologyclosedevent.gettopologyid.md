---
navigation:
  - class.mongodb-driver-monitoring-topologyclosedevent.md: « MongoDBDriverMonitoringTopologyClosedEvent
  - class.mongodb-driver-monitoring-topologyopeningevent.md: MongoDBDriverMonitoringTopologyOpeningEvent »
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-topologyclosedevent.md: MongoDBDriverMonitoringTopologyClosedEvent
title: 'MongoDBDriverMonitoringTopologyClosedEvent::getTopologyId'
---
# MongoDBDriverMonitoringTopologyClosedEvent::getTopologyId

(mongodb >=1.13.0)

MongoDBDriverMonitoringTopologyClosedEvent::getTopologyId — Повертає ідентифікатор топології

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\TopologyClosedEvent::getTopologyId(): MongoDB\BSON\ObjectId
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор топології.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
