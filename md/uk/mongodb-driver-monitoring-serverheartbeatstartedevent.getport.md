---
navigation:
  - mongodb-driver-monitoring-serverheartbeatstartedevent.gethost.md: '« MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent::getHost'
  - mongodb-driver-monitoring-serverheartbeatstartedevent.isawaited.md: 'MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent::isAwaited »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverheartbeatstartedevent.md: MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent
title: 'MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent::getPort'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent::getPort

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent::getPort — Повертає порт, на якому прослуховується сервер

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerHeartbeatStartedEvent::getPort(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає порт, у якому прослуховується сервер.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
