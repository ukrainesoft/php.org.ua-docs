---
navigation:
  - mongodb-driver-monitoring-serverheartbeatstartedevent.getport.html: '« MongoDBDriverMonitoringServerHeartbeatStartedEvent::getPort'
  - class.mongodb-driver-monitoring-serverheartbeatsucceededevent.html: MongoDBDriverMonitoringServerHeartbeatSucceededEvent »
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverheartbeatstartedevent.html: MongoDBDriverMonitoringServerHeartbeatStartedEvent
title: 'MongoDBDriverMonitoringServerHeartbeatStartedEvent::isAwaited'
---
# MongoDBDriverMonitoringServerHeartbeatStartedEvent::isAwaited

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerHeartbeatStartedEvent::isAwaited — Повертає, чи використовувався в heartbeat потоковий протокол

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerHeartbeatStartedEvent::isAwaited(): bool
```

Повертає, чи використовувався в heartbeat потоковий протокол. Драйвер PHP не використовує потоковий протокол для моніторингу, тому цей метод завжди повертатиметься **`false`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`false`**

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
