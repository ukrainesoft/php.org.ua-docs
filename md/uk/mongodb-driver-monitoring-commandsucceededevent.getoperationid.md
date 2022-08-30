Повертає ідентифікатор операції команди

-   [« MongoDBDriverMonitoringCommandSucceededEvent::getDurationMicros](mongodb-driver-monitoring-commandsucceededevent.getdurationmicros.html)
    
-   [MongoDBDriverMonitoringCommandSucceededEvent::getReply »](mongodb-driver-monitoring-commandsucceededevent.getreply.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverMonitoringCommandSucceededEvent](class.mongodb-driver-monitoring-commandsucceededevent.html)
    
-   Повертає ідентифікатор операції команди
    

# MongoDBDriverMonitoringCommandSucceededEvent::getOperationId

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandSucceededEvent::getOperationId — Повертає ідентифікатор операції команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandSucceededEvent::getOperationId(): string
```

Ідентифікатор операції генерується драйвером і може бути використаний для зв'язування подій разом, таких як операцій масового запису, які можуть бути розділені на кілька команд на рівні протоколу.

> **Зауваження**: Оскільки кілька команд можуть спільно використовувати той самий ідентифікатор операції, недоцільно використовувати його для зв'язування об'єктів подій один з одним. Натомість слід використовувати ідентифікатор запиту, повернутий [MongoDBDriverMonitoringCommandSucceededEvent::getRequestId()](mongodb-driver-monitoring-commandsucceededevent.getrequestid.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор операції команди.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverMonitoringCommandStartedEvent::getOperationId()](mongodb-driver-monitoring-commandstartedevent.getoperationid.html) - Повертає ідентифікатор операції команди
-   [MongoDBDriverMonitoringCommandSucceededEvent::getRequestId()](mongodb-driver-monitoring-commandsucceededevent.getrequestid.html) - Повертає ідентифікатор запиту команди
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.html)