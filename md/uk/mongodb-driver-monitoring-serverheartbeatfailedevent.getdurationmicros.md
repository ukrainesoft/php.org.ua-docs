---
navigation:
  - class.mongodb-driver-monitoring-serverheartbeatfailedevent.md: « MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent
  - mongodb-driver-monitoring-serverheartbeatfailedevent.geterror.md: 'MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::getError »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverheartbeatfailedevent.md: MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent
title: 'MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::getDurationMicros'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::getDurationMicros

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::getDurationMicros — Повертає тривалість heartbeat у мікросекундах

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

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
