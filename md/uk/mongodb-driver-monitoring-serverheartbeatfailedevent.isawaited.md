---
navigation:
  - mongodb-driver-monitoring-serverheartbeatfailedevent.getport.md: '« MongoDBDriverMonitoringServerHeartbeatFailedEvent::getPort'
  - class.mongodb-driver-monitoring-serverheartbeatstartedevent.md: MongoDBDriverMonitoringServerHeartbeatStartedEvent »
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverheartbeatfailedevent.md: MongoDBDriverMonitoringServerHeartbeatFailedEvent
title: 'MongoDBDriverMonitoringServerHeartbeatFailedEvent::isAwaited'
---
# MongoDBDriverMonitoringServerHeartbeatFailedEvent::isAwaited

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerHeartbeatFailedEvent::isAwaited — Повертає, чи використовувався в heartbeat потоковий протокол

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerHeartbeatFailedEvent::isAwaited(): bool
```

Повертає, чи використовувався в heartbeat потоковий протокол. Драйвер PHP не використовує потоковий протокол для моніторингу, тому цей метод завжди повертатиметься **`false`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`false`**

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
