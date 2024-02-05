---
navigation:
  - mongodb-driver-monitoring-commandfailedevent.getoperationid.md: '« MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getOperationId'
  - mongodb-driver-monitoring-commandfailedevent.getrequestid.md: 'MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getRequestId »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandfailedevent.md: MongoDB\\Driver\\Monitoring\\CommandFailedEvent
title: 'MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getReply'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getReply

(mongodb >=1.5.0)

MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getReply — Повертає документ відповіді команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandFailedEvent::getReply(): object
```

У відповідь документ буде перетворено з BSON в PHP з використанням правил [десеріалізації](mongodb.persistence.deserialization.md) за промовчанням (наприклад, документи BSON будуть перетворені на [stdClass](class.stdclass.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає документ відповіді команди у вигляді об'єкту [stdClass](class.stdclass.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
-   [Постійні дані](mongodb.persistence.md)
