---
navigation:
  - mongodb-driver-monitoring-serverchangedevent.gethost.html: '« MongoDBDriverMonitoringServerChangedEvent::getHost'
  - mongodb-driver-monitoring-serverchangedevent.getport.html: 'MongoDBDriverMonitoringServerChangedEvent::getPort »'
  - index.html: PHP Manual
  - class.mongodb-driver-monitoring-serverchangedevent.html: MongoDBDriverMonitoringServerChangedEvent
title: 'MongoDBDriverMonitoringServerChangedEvent::getNewDescription'
---
# MongoDBDriverMonitoringServerChangedEvent::getNewDescription

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerChangedEvent::getNewDescription — Повертає новий опис сервера

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerChangedEvent::getNewDescription(): MongoDB\Driver\ServerDescription
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає новий опис ([MongoDBDriverServerDescription](class.mongodb-driver-serverdescription.md)) сервера.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
