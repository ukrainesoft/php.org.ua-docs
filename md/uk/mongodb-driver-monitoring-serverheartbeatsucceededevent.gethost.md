---
navigation:
  - mongodb-driver-monitoring-serverheartbeatsucceededevent.getdurationmicros.md: '« MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getDurationMicros'
  - mongodb-driver-monitoring-serverheartbeatsucceededevent.getport.md: 'MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getPort »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverheartbeatsucceededevent.md: MongoDBDriverMonitoringServerHeartbeatSucceededEvent
title: 'MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getHost'
---
# MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getHost

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getHost — Повертає ім'я сервера.

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerHeartbeatSucceededEvent::getHost(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я сервера хоста.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
