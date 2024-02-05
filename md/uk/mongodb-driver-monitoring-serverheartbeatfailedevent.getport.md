---
navigation:
  - mongodb-driver-monitoring-serverheartbeatfailedevent.gethost.md: '« MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::getHost'
  - mongodb-driver-monitoring-serverheartbeatfailedevent.isawaited.md: 'MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::isAwaited »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverheartbeatfailedevent.md: MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent
title: 'MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::getPort'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::getPort

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::getPort — Повертає порт, на якому прослуховується сервер

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerHeartbeatFailedEvent::getPort(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає порт, у якому прослуховується сервер.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
