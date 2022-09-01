---
navigation:
  - mongodb-driver-monitoring-serverheartbeatfailedevent.gethost.html: '« MongoDBDriverMonitoringServerHeartbeatFailedEvent::getHost'
  - mongodb-driver-monitoring-serverheartbeatfailedevent.isawaited.html: 'MongoDBDriverMonitoringServerHeartbeatFailedEvent::isAwaited »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverheartbeatfailedevent.html: MongoDBDriverMonitoringServerHeartbeatFailedEvent
title: 'MongoDBDriverMonitoringServerHeartbeatFailedEvent::getPort'
---
# MongoDBDriverMonitoringServerHeartbeatFailedEvent::getPort

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerHeartbeatFailedEvent::getPort — Повертає порт, на якому прослуховується сервер

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerHeartbeatFailedEvent::getPort(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає порт, у якому прослуховується сервер.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
