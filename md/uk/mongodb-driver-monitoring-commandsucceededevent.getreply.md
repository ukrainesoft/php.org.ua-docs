---
navigation:
  - mongodb-driver-monitoring-commandsucceededevent.getoperationid.md: '« MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getOperationId'
  - mongodb-driver-monitoring-commandsucceededevent.getrequestid.md: 'MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getRequestId »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandsucceededevent.md: MongoDB\\Driver\\Monitoring\\CommandSucceededEvent
title: 'MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getReply'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getReply

(mongodb >=1.3.0)

MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getReply — Повертає документ відповіді команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandSucceededEvent::getReply(): object
```

Документ ответа будет преобразован из BSON в PHP с использованием правил[десеріалізації](mongodb.persistence.deserialization.md) (наприклад, документи BSON будуть перетворені на [stdClass](class.stdclass.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає документ відповіді команди у вигляді об'єкту [stdClass](class.stdclass.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
-   [Постійні дані](mongodb.persistence.md)
