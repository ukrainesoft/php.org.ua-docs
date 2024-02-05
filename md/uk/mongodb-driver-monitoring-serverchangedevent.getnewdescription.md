---
navigation:
  - mongodb-driver-monitoring-serverchangedevent.gethost.md: '« MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getHost'
  - mongodb-driver-monitoring-serverchangedevent.getport.md: 'MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getPort »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverchangedevent.md: MongoDB\\Driver\\Monitoring\\ServerChangedEvent
title: 'MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getNewDescription'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getNewDescription

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getNewDescription — Повертає новий опис сервера

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerChangedEvent::getNewDescription(): MongoDB\Driver\ServerDescription
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає новий опис ([MongoDB\\Driver\\ServerDescription](class.mongodb-driver-serverdescription.md)) сервера.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
