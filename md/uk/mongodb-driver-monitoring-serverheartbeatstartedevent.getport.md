---
navigation:
  - mongodb-driver-monitoring-serverheartbeatstartedevent.gethost.html: '« MongoDBDriverMonitoringServerHeartbeatStartedEvent::getHost'
  - mongodb-driver-monitoring-serverheartbeatstartedevent.isawaited.html: 'MongoDBDriverMonitoringServerHeartbeatStartedEvent::isAwaited »'
  - index.html: PHP Manual
  - class.mongodb-driver-monitoring-serverheartbeatstartedevent.html: MongoDBDriverMonitoringServerHeartbeatStartedEvent
title: 'MongoDBDriverMonitoringServerHeartbeatStartedEvent::getPort'
---
# MongoDBDriverMonitoringServerHeartbeatStartedEvent::getPort

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerHeartbeatStartedEvent::getPort — Повертає порт, на якому прослуховується сервер

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerHeartbeatStartedEvent::getPort(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає порт, у якому прослуховується сервер.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
