---
navigation:
  - class.mongodb-driver-monitoring-serverclosedevent.md: « MongoDB\\Driver\\Monitoring\\ServerClosedEvent
  - mongodb-driver-monitoring-serverclosedevent.getport.md: 'MongoDB\\Driver\\Monitoring\\ServerClosedEvent::getPort »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverclosedevent.md: MongoDB\\Driver\\Monitoring\\ServerClosedEvent
title: 'MongoDB\\Driver\\Monitoring\\ServerClosedEvent::getHost'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\ServerClosedEvent::getHost

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\ServerClosedEvent::getHost — Повертає ім'я сервера.

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerClosedEvent::getHost(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я сервера хоста.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
