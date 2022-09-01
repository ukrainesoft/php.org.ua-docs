---
navigation:
  - mongodb-driver-monitoring-serverchangedevent.getport.html: '« MongoDBDriverMonitoringServerChangedEvent::getPort'
  - mongodb-driver-monitoring-serverchangedevent.gettopologyid.html: 'MongoDBDriverMonitoringServerChangedEvent::getTopologyId »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverchangedevent.html: MongoDBDriverMonitoringServerChangedEvent
title: 'MongoDBDriverMonitoringServerChangedEvent::getPreviousDescription'
---
# MongoDBDriverMonitoringServerChangedEvent::getPreviousDescription

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerChangedEvent::getPreviousDescription — Повертає попередній опис сервера

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerChangedEvent::getPreviousDescription(): MongoDB\Driver\ServerDescription
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає попередній опис ([MongoDBDriverServerDescription](class.mongodb-driver-serverdescription.md)) сервера.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
