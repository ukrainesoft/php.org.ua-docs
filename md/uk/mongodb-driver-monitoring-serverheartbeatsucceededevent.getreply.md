---
navigation:
  - mongodb-driver-monitoring-serverheartbeatsucceededevent.getport.md: '« MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getPort'
  - mongodb-driver-monitoring-serverheartbeatsucceededevent.isawaited.md: 'MongoDBDriverMonitoringServerHeartbeatSucceededEvent::isAwaited »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-serverheartbeatsucceededevent.md: MongoDBDriverMonitoringServerHeartbeatSucceededEvent
title: 'MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getReply'
---
# MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getReply

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getReply — Повертає документ відповіді heartbeat

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerHeartbeatSucceededEvent::getReply(): object
```

Документ відповіді буде перетворено з BSON на PHP з використанням правил [десериализации](mongodb.persistence.deserialization.md) за промовчанням (наприклад, документи BSON будуть перетворені на stdClass).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає документ відповіді heartbeat у вигляді об'єкта **stdClass**

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
-   [Постійні дані](mongodb.persistence.md)
