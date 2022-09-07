---
navigation:
  - mongodb-driver-monitoring-serverheartbeatfailedevent.geterror.md: '« MongoDBDriverMonitoringServerHeartbeatFailedEvent::getError'
  - mongodb-driver-monitoring-serverheartbeatfailedevent.getport.md: 'MongoDBDriverMonitoringServerHeartbeatFailedEvent::getPort »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverheartbeatfailedevent.md: MongoDBDriverMonitoringServerHeartbeatFailedEvent
title: 'MongoDBDriverMonitoringServerHeartbeatFailedEvent::getHost'
---
# MongoDBDriverMonitoringServerHeartbeatFailedEvent::getHost

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerHeartbeatFailedEvent::getHost — Повертає ім'я сервера.

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerHeartbeatFailedEvent::getHost(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я сервера хоста.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
