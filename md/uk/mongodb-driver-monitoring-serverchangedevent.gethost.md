---
navigation:
  - class.mongodb-driver-monitoring-serverchangedevent.md: « MongoDB\\Driver\\Monitoring\\ServerChangedEvent
  - mongodb-driver-monitoring-serverchangedevent.getnewdescription.md: 'MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getNewDescription »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverchangedevent.md: MongoDB\\Driver\\Monitoring\\ServerChangedEvent
title: 'MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getHost'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getHost

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getHost — Повертає ім'я сервера.

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerChangedEvent::getHost(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я сервера хоста.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
