---
navigation:
  - class.mongodb-driver-monitoring-serveropeningevent.md: « MongoDBDriverMonitoringServerOpeningEvent
  - mongodb-driver-monitoring-serveropeningevent.getport.md: 'MongoDBDriverMonitoringServerOpeningEvent::getPort »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serveropeningevent.md: MongoDBDriverMonitoringServerOpeningEvent
title: 'MongoDBDriverMonitoringServerOpeningEvent::getHost'
---
# MongoDBDriverMonitoringServerOpeningEvent::getHost

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerOpeningEvent::getHost — Повертає ім'я сервера.

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerOpeningEvent::getHost(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я сервера хоста.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
