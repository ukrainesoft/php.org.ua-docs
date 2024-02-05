---
navigation:
  - mongodb-driver-monitoring-commandstartedevent.getdatabasename.md: '« MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getDatabaseName'
  - mongodb-driver-monitoring-commandstartedevent.getrequestid.md: 'MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getRequestId »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandstartedevent.md: MongoDB\\Driver\\Monitoring\\CommandStartedEvent
title: 'MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getOperationId'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getOperationId

(mongodb >=1.3.0)

MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getOperationId — Повертає ідентифікатор операції команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandStartedEvent::getOperationId(): string
```

Ідентифікатор операції генерується драйвером і може бути використаний для зв'язування подій разом, таких як операцій масового запису, які можуть бути розділені на кілька команд на рівні протоколу.

> **Зауваження**: Оскільки кілька команд можуть спільно використовувати той самий ідентифікатор операції, недоцільно використовувати його для зв'язування об'єктів подій один з одним. Натомість слід використовувати ідентифікатор запиту, повернутий [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getRequestId()](mongodb-driver-monitoring-commandstartedevent.getrequestid.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор операції команди.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getOperationId()](mongodb-driver-monitoring-commandfailedevent.getoperationid.md) \- Повертає ідентифікатор операції команди
-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getOperationId()](mongodb-driver-monitoring-commandsucceededevent.getoperationid.md) \- Повертає ідентифікатор операції команди
-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getRequestId()](mongodb-driver-monitoring-commandstartedevent.getrequestid.md) \- Повертає ідентифікатор запиту команди
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
