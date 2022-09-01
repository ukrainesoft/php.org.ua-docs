---
navigation:
  - mongodb-driver-monitoring-commandfailedevent.getoperationid.html: '« MongoDBDriverMonitoringCommandFailedEvent::getOperationId'
  - mongodb-driver-monitoring-commandfailedevent.getrequestid.html: 'MongoDBDriverMonitoringCommandFailedEvent::getRequestId »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandfailedevent.html: MongoDBDriverMonitoringCommandFailedEvent
title: 'MongoDBDriverMonitoringCommandFailedEvent::getReply'
---
# MongoDBDriverMonitoringCommandFailedEvent::getReply

(mongodb >=1.5.0)

MongoDBDriverMonitoringCommandFailedEvent::getReply — Повертає документ відповіді команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandFailedEvent::getReply(): object
```

У відповідь документ буде перетворено з BSON в PHP з використанням правил [десериализации](mongodb.persistence.deserialization.md) за промовчанням (наприклад, документи BSON будуть перетворені на stdClass).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає документ відповіді команди у вигляді об'єкту **stdClass**

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
-   [Постійні дані](mongodb.persistence.md)
