---
navigation:
  - mongodb-driver-monitoring-serverclosedevent.getport.md: '« MongoDBDriverMonitoringServerClosedEvent::getPort'
  - class.mongodb-driver-monitoring-serveropeningevent.md: MongoDBDriverMonitoringServerOpeningEvent »
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverclosedevent.md: MongoDBDriverMonitoringServerClosedEvent
title: 'MongoDBDriverMonitoringServerClosedEvent::getTopologyId'
---
# MongoDBDriverMonitoringServerClosedEvent::getTopologyId

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerClosedEvent::getTopologyId — Повертає ідентифікатор топології, пов'язаний із цим сервером

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerClosedEvent::getTopologyId(): MongoDB\BSON\ObjectId
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор топології.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
