Повертає ідентифікатор операції команди

-   [« MongoDBDriverMonitoringCommandStartedEvent::getDatabaseName](mongodb-driver-monitoring-commandstartedevent.getdatabasename.html)
    
-   [MongoDBDriverMonitoringCommandStartedEvent::getRequestId »](mongodb-driver-monitoring-commandstartedevent.getrequestid.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverMonitoringCommandStartedEvent](class.mongodb-driver-monitoring-commandstartedevent.html)
    
-   Повертає ідентифікатор операції команди
    

# MongoDBDriverMonitoringCommandStartedEvent::getOperationId

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandStartedEvent::getOperationId — Повертає ідентифікатор операції команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandStartedEvent::getOperationId(): string
```

Ідентифікатор операції генерується драйвером і може бути використаний для зв'язування подій разом, таких як операцій масового запису, які можуть бути розділені на кілька команд на рівні протоколу.

> **Зауваження**: Оскільки кілька команд можуть спільно використовувати той самий ідентифікатор операції, недоцільно використовувати його для зв'язування об'єктів подій один з одним. Натомість слід використовувати ідентифікатор запиту, повернутий [MongoDBDriverMonitoringCommandStartedEvent::getRequestId()](mongodb-driver-monitoring-commandstartedevent.getrequestid.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор операції команди.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverMonitoringCommandFailedEvent::getOperationId()](mongodb-driver-monitoring-commandfailedevent.getoperationid.html) - Повертає ідентифікатор операції команди
-   [MongoDBDriverMonitoringCommandSucceededEvent::getOperationId()](mongodb-driver-monitoring-commandsucceededevent.getoperationid.html) - Повертає ідентифікатор операції команди
-   [MongoDBDriverMonitoringCommandStartedEvent::getRequestId()](mongodb-driver-monitoring-commandstartedevent.getrequestid.html) - Повертає ідентифікатор запиту команди
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)