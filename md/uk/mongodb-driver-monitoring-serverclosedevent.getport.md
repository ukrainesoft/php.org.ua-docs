---
navigation:
  - mongodb-driver-monitoring-serverclosedevent.gethost.html: '« MongoDBDriverMonitoringServerClosedEvent::getHost'
  - mongodb-driver-monitoring-serverclosedevent.gettopologyid.html: 'MongoDBDriverMonitoringServerClosedEvent::getTopologyId »'
  - index.html: PHP Manual
  - class.mongodb-driver-monitoring-serverclosedevent.html: MongoDBDriverMonitoringServerClosedEvent
title: 'MongoDBDriverMonitoringServerClosedEvent::getPort'
---
# MongoDBDriverMonitoringServerClosedEvent::getPort

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerClosedEvent::getPort — Повертає порт, на якому прослуховується сервер

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerClosedEvent::getPort(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає порт, у якому прослуховується сервер.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
