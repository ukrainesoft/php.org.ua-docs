---
navigation:
  - mongodb-driver-monitoring-serverheartbeatfailedevent.getdurationmicros.html: '« MongoDBDriverMonitoringServerHeartbeatFailedEvent::getDurationMicros'
  - mongodb-driver-monitoring-serverheartbeatfailedevent.gethost.html: 'MongoDBDriverMonitoringServerHeartbeatFailedEvent::getHost »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverheartbeatfailedevent.html: MongoDBDriverMonitoringServerHeartbeatFailedEvent
title: 'MongoDBDriverMonitoringServerHeartbeatFailedEvent::getError'
---
# MongoDBDriverMonitoringServerHeartbeatFailedEvent::getError

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerHeartbeatFailedEvent::getError — Повертає виняток, пов'язаний із невдалим виконанням heartbeat

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerHeartbeatFailedEvent::getError(): Exception
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає виняток ([Exception](class.exception.md)), пов'язане з невдалим виконанням heartbeat.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
