---
navigation:
  - class.mongodb-driver-monitoring-commandstartedevent.md: « MongoDBDriverMonitoringCommandStartedEvent
  - mongodb-driver-monitoring-commandstartedevent.getcommandname.md: 'MongoDBDriverMonitoringCommandStartedEvent::getCommandName »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandstartedevent.md: MongoDBDriverMonitoringCommandStartedEvent
title: 'MongoDBDriverMonitoringCommandStartedEvent::getCommand'
---
# MongoDBDriverMonitoringCommandStartedEvent::getCommand

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandStartedEvent::getCommand — Повертає документ команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandStartedEvent::getCommand(): object
```

Документ відповіді буде перетворено з BSON в PHP, використовуючи правила [десериализации](mongodb.persistence.deserialization.md) (наприклад, документи BSON будуть перетворені на stdClass).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає документ команди у вигляді об'єкту **stdClass**

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
-   [Постійні дані](mongodb.persistence.md)
