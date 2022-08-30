Повертає ідентифікатор операції команди

-   [« MongoDBDriverMonitoringCommandFailedEvent::getError](mongodb-driver-monitoring-commandfailedevent.geterror.html)
    
-   [MongoDBDriverMonitoringCommandFailedEvent::getReply »](mongodb-driver-monitoring-commandfailedevent.getreply.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverMonitoringCommandFailedEvent](class.mongodb-driver-monitoring-commandfailedevent.html)
    
-   Повертає ідентифікатор операції команди
    

# MongoDBDriverMonitoringCommandFailedEvent::getOperationId

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandFailedEvent::getOperationId — Повертає ідентифікатор операції команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandFailedEvent::getOperationId(): string
```

Ідентифікатор операції генерується драйвером і може бути використаний для зв'язування подій разом, таких як операцій масового запису, які можуть бути розділені на кілька команд на рівні протоколу.

> **Зауваження**: Оскільки кілька команд можуть спільно використовувати той самий ідентифікатор операції, недоцільно використовувати його для зв'язування об'єктів подій один з одним. Натомість слід використовувати ідентифікатор запиту, повернутий [MongoDBDriverMonitoringCommandFailedEvent::getRequestId()](mongodb-driver-monitoring-commandfailedevent.getrequestid.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор операції команди.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverMonitoringCommandStartedEvent::getOperationId()](mongodb-driver-monitoring-commandstartedevent.getoperationid.html) - Повертає ідентифікатор операції команди
-   [MongoDBDriverMonitoringCommandFailedEvent::getRequestId()](mongodb-driver-monitoring-commandfailedevent.getrequestid.html) - Повертає ідентифікатор запиту команди
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.html)