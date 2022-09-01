---
navigation:
  - class.mongodb-driver-monitoring-serverheartbeatfailedevent.html: « MongoDBDriverMonitoringServerHeartbeatFailedEvent
  - mongodb-driver-monitoring-serverheartbeatfailedevent.geterror.html: 'MongoDBDriverMonitoringServerHeartbeatFailedEvent::getError »'
  - index.html: PHP Manual
  - class.mongodb-driver-monitoring-serverheartbeatfailedevent.html: MongoDBDriverMonitoringServerHeartbeatFailedEvent
title: 'MongoDBDriverMonitoringServerHeartbeatFailedEvent::getDurationMicros'
---
# MongoDBDriverMonitoringServerHeartbeatFailedEvent::getDurationMicros

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerHeartbeatFailedEvent::getDurationMicros — Повертає тривалість heartbeat у мікросекундах

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerHeartbeatFailedEvent::getDurationMicros(): int
```

Тривалість heartbeat - це розрахункове значення, яке включає час відправки повідомлення і отримання відповіді від сервера.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає тривалість heartbeat в мікросекундах.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
