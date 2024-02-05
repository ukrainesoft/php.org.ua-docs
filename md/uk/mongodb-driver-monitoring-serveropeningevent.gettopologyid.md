---
navigation:
  - mongodb-driver-monitoring-serveropeningevent.getport.md: '« MongoDB\\Driver\\Monitoring\\ServerOpeningEvent::getPort'
  - class.mongodb-driver-monitoring-serverheartbeatfailedevent.md: MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent »
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serveropeningevent.md: MongoDB\\Driver\\Monitoring\\ServerOpeningEvent
title: 'MongoDB\\Driver\\Monitoring\\ServerOpeningEvent::getTopologyId'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\ServerOpeningEvent::getTopologyId

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\ServerOpeningEvent::getTopologyId — Returns the topology ID associated with this server

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerOpeningEvent::getTopologyId(): MongoDB\BSON\ObjectId
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Returns the topology ID.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
