---
navigation:
  - mongodb-driver-monitoring-serveropeningevent.gethost.html: '« MongoDBDriverMonitoringServerOpeningEvent::getHost'
  - mongodb-driver-monitoring-serveropeningevent.gettopologyid.html: 'MongoDBDriverMonitoringServerOpeningEvent::getTopologyId »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serveropeningevent.html: MongoDBDriverMonitoringServerOpeningEvent
title: 'MongoDBDriverMonitoringServerOpeningEvent::getPort'
---
# MongoDBDriverMonitoringServerOpeningEvent::getPort

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerOpeningEvent::getPort — Повертає порт, на якому прослуховується сервер

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerOpeningEvent::getPort(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає порт, у якому прослуховується сервер.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
