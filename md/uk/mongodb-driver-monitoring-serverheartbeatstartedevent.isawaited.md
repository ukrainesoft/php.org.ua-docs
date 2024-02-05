---
navigation:
  - mongodb-driver-monitoring-serverheartbeatstartedevent.getport.md: '« MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent::getPort'
  - class.mongodb-driver-monitoring-serverheartbeatsucceededevent.md: MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent »
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverheartbeatstartedevent.md: MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent
title: 'MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent::isAwaited'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent::isAwaited

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent::isAwaited — Повертає, чи використовувався в heartbeat потоковий протокол

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

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
