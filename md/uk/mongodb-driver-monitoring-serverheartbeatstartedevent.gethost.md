---
navigation:
  - class.mongodb-driver-monitoring-serverheartbeatstartedevent.md: « MongoDBDriverMonitoringServerHeartbeatStartedEvent
  - mongodb-driver-monitoring-serverheartbeatstartedevent.getport.md: 'MongoDBDriverMonitoringServerHeartbeatStartedEvent::getPort »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverheartbeatstartedevent.md: MongoDBDriverMonitoringServerHeartbeatStartedEvent
title: 'MongoDBDriverMonitoringServerHeartbeatStartedEvent::getHost'
---
# MongoDBDriverMonitoringServerHeartbeatStartedEvent::getHost

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerHeartbeatStartedEvent::getHost — Повертає ім'я сервера.

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerHeartbeatStartedEvent::getHost(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я сервера хоста.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
