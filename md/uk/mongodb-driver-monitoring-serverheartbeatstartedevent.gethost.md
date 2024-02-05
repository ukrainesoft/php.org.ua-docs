---
navigation:
  - class.mongodb-driver-monitoring-serverheartbeatstartedevent.md: « MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent
  - mongodb-driver-monitoring-serverheartbeatstartedevent.getport.md: 'MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent::getPort »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverheartbeatstartedevent.md: MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent
title: 'MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent::getHost'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent::getHost

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent::getHost — Повертає ім'я сервера.

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerHeartbeatStartedEvent::getHost(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я сервера хоста.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
