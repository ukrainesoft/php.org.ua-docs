---
navigation:
  - mongodb-driver-monitoring-serverheartbeatsucceededevent.gethost.md: '« MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getHost'
  - mongodb-driver-monitoring-serverheartbeatsucceededevent.getreply.md: 'MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getReply »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverheartbeatsucceededevent.md: MongoDBDriverMonitoringServerHeartbeatSucceededEvent
title: 'MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getPort'
---
# MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getPort

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getPort — Повертає порт, на якому прослуховується сервер

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerHeartbeatSucceededEvent::getPort(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає порт, у якому прослуховується сервер.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
