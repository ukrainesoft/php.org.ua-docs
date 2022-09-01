---
navigation:
  - class.mongodb-driver-monitoring-serverheartbeatsucceededevent.html: « MongoDBDriverMonitoringServerHeartbeatSucceededEvent
  - mongodb-driver-monitoring-serverheartbeatsucceededevent.gethost.html: 'MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getHost »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverheartbeatsucceededevent.html: MongoDBDriverMonitoringServerHeartbeatSucceededEvent
title: 'MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getDurationMicros'
---
# MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getDurationMicros

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getDurationMicros — Повертає тривалість heartbeat у мікросекундах

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerHeartbeatSucceededEvent::getDurationMicros(): int
```

Тривалість heartbeat - це розрахункове значення, яке включає час відправки повідомлення і отримання відповіді від сервера.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає тривалість heartbeat в мікросекундах.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
