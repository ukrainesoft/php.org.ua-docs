---
navigation:
  - mongodb-driver-monitoring-serveropeningevent.getport.md: '« MongoDBDriverMonitoringServerOpeningEvent::getPort'
  - class.mongodb-driver-monitoring-serverheartbeatfailedevent.md: MongoDBDriverMonitoringServerHeartbeatFailedEvent »
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serveropeningevent.md: MongoDBDriverMonitoringServerOpeningEvent
title: 'MongoDBDriverMonitoringServerOpeningEvent::getTopologyId'
---
# MongoDBDriverMonitoringServerOpeningEvent::getTopologyId

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerOpeningEvent::getTopologyId — Returns the topology ID associated with this server

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerOpeningEvent::getTopologyId(): MongoDB\BSON\ObjectId
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Відображення топології ID.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
