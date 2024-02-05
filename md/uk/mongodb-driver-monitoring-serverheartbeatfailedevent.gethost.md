---
navigation:
  - mongodb-driver-monitoring-serverheartbeatfailedevent.geterror.md: '« MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::getError'
  - mongodb-driver-monitoring-serverheartbeatfailedevent.getport.md: 'MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::getPort »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverheartbeatfailedevent.md: MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent
title: 'MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::getHost'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::getHost

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::getHost — Повертає ім'я сервера.

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerHeartbeatFailedEvent::getHost(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я сервера хоста.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
