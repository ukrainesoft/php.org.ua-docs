---
navigation:
  - mongodb-driver-monitoring-serverheartbeatsucceededevent.gethost.md: '« MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::getHost'
  - mongodb-driver-monitoring-serverheartbeatsucceededevent.getreply.md: 'MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::getReply »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverheartbeatsucceededevent.md: MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent
title: 'MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::getPort'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::getPort

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::getPort — Повертає порт, на якому прослуховується сервер

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerHeartbeatSucceededEvent::getPort(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає порт, у якому прослуховується сервер.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
