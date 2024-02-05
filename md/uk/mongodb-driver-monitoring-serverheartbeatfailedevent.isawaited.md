---
navigation:
  - mongodb-driver-monitoring-serverheartbeatfailedevent.getport.md: '« MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::getPort'
  - class.mongodb-driver-monitoring-serverheartbeatstartedevent.md: MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent »
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverheartbeatfailedevent.md: MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent
title: 'MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::isAwaited'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::isAwaited

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::isAwaited — Повертає, чи використовувався в heartbeat потоковий протокол

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

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
