---
navigation:
  - mongodb-driver-monitoring-serverheartbeatfailedevent.getdurationmicros.md: >-
      «
      MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::getDurationMicros
  - mongodb-driver-monitoring-serverheartbeatfailedevent.gethost.md: 'MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::getHost »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverheartbeatfailedevent.md: MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent
title: 'MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::getError'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::getError

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::getError — Повертає виняток, пов'язаний із невдалим виконанням heartbeat

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerHeartbeatFailedEvent::getError(): Exception
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає виняток ([Exception](class.exception.md)), пов'язане з невдалим виконанням heartbeat.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
