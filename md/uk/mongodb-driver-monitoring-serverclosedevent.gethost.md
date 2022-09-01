---
navigation:
  - class.mongodb-driver-monitoring-serverclosedevent.html: « MongoDBDriverMonitoringServerClosedEvent
  - mongodb-driver-monitoring-serverclosedevent.getport.html: 'MongoDBDriverMonitoringServerClosedEvent::getPort »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverclosedevent.html: MongoDBDriverMonitoringServerClosedEvent
title: 'MongoDBDriverMonitoringServerClosedEvent::getHost'
---
# MongoDBDriverMonitoringServerClosedEvent::getHost

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerClosedEvent::getHost — Повертає ім'я сервера.

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerClosedEvent::getHost(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я сервера хоста.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
