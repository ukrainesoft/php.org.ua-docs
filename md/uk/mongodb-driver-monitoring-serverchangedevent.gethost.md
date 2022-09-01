---
navigation:
  - class.mongodb-driver-monitoring-serverchangedevent.html: « MongoDBDriverMonitoringServerChangedEvent
  - mongodb-driver-monitoring-serverchangedevent.getnewdescription.html: 'MongoDBDriverMonitoringServerChangedEvent::getNewDescription »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverchangedevent.html: MongoDBDriverMonitoringServerChangedEvent
title: 'MongoDBDriverMonitoringServerChangedEvent::getHost'
---
# MongoDBDriverMonitoringServerChangedEvent::getHost

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerChangedEvent::getHost — Повертає ім'я сервера.

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerChangedEvent::getHost(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я сервера хоста.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
