---
navigation:
  - mongodb-driver-monitoring-serverheartbeatsucceededevent.getdurationmicros.md: >-
      «
      MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::getDurationMicros
  - mongodb-driver-monitoring-serverheartbeatsucceededevent.getport.md: 'MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::getPort »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverheartbeatsucceededevent.md: MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent
title: 'MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::getHost'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::getHost

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::getHost — Повертає ім'я сервера.

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerHeartbeatSucceededEvent::getHost(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я сервера хоста.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
