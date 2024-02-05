---
navigation:
  - class.mongodb-driver-monitoring-commandstartedevent.md: « MongoDB\\Driver\\Monitoring\\CommandStartedEvent
  - mongodb-driver-monitoring-commandstartedevent.getcommandname.md: 'MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getCommandName »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandstartedevent.md: MongoDB\\Driver\\Monitoring\\CommandStartedEvent
title: 'MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getCommand'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getCommand

(mongodb >=1.3.0)

MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getCommand — Повертає документ команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandStartedEvent::getCommand(): object
```

Документ ответа будет преобразован из BSON в PHP используя правила[десеріалізації](mongodb.persistence.deserialization.md) (наприклад, документи BSON будуть перетворені на [stdClass](class.stdclass.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає документ команди у вигляді об'єкту [stdClass](class.stdclass.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
-   [Постійні дані](mongodb.persistence.md)
