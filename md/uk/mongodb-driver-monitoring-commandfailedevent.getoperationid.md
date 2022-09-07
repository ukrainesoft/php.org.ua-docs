---
navigation:
  - mongodb-driver-monitoring-commandfailedevent.geterror.md: '« MongoDBDriverMonitoringCommandFailedEvent::getError'
  - mongodb-driver-monitoring-commandfailedevent.getreply.md: 'MongoDBDriverMonitoringCommandFailedEvent::getReply »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandfailedevent.md: MongoDBDriverMonitoringCommandFailedEvent
title: 'MongoDBDriverMonitoringCommandFailedEvent::getOperationId'
---
# MongoDBDriverMonitoringCommandFailedEvent::getOperationId

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandFailedEvent::getOperationId — Повертає ідентифікатор операції команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandFailedEvent::getOperationId(): string
```

Ідентифікатор операції генерується драйвером і може бути використаний для зв'язування подій разом, таких як операцій масового запису, які можуть бути розділені на кілька команд на рівні протоколу.

> **Зауваження**: Оскільки кілька команд можуть спільно використовувати той самий ідентифікатор операції, недоцільно використовувати його для зв'язування об'єктів подій один з одним. Натомість слід використовувати ідентифікатор запиту, повернутий [MongoDBDriverMonitoringCommandFailedEvent::getRequestId()](mongodb-driver-monitoring-commandfailedevent.getrequestid.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор операції команди.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverMonitoringCommandStartedEvent::getOperationId()](mongodb-driver-monitoring-commandstartedevent.getoperationid.md) - Повертає ідентифікатор операції команди
-   [MongoDBDriverMonitoringCommandFailedEvent::getRequestId()](mongodb-driver-monitoring-commandfailedevent.getrequestid.md) - Повертає ідентифікатор запиту команди
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
