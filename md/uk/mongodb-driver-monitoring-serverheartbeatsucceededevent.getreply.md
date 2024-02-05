---
navigation:
  - mongodb-driver-monitoring-serverheartbeatsucceededevent.getport.md: '« MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::getPort'
  - mongodb-driver-monitoring-serverheartbeatsucceededevent.isawaited.md: 'MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::isAwaited »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverheartbeatsucceededevent.md: MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent
title: 'MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::getReply'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::getReply

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::getReply — Повертає документ відповіді heartbeat

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerHeartbeatSucceededEvent::getReply(): object
```

Документ ответа будет преобразован из BSON в PHP с использованием правил[десеріалізації](mongodb.persistence.deserialization.md) за промовчанням (наприклад, документи BSON будуть перетворені на [stdClass](class.stdclass.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає документ відповіді heartbeat у вигляді об'єкта [stdClass](class.stdclass.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
-   [Постійні дані](mongodb.persistence.md)
