---
navigation:
  - mongodb-driver-monitoring-serverchangedevent.getnewdescription.md: '« MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getNewDescription'
  - mongodb-driver-monitoring-serverchangedevent.getpreviousdescription.md: 'MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getPreviousDescription »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverchangedevent.md: MongoDB\\Driver\\Monitoring\\ServerChangedEvent
title: 'MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getPort'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getPort

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getPort — Повертає порт, на якому прослуховується сервер

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerChangedEvent::getPort(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає порт, у якому прослуховується сервер.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
