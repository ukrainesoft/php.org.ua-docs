Повертає ідентифікатор операції команди

-   [« MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getDatabaseName](mongodb-driver-monitoring-commandstartedevent.getdatabasename.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getRequestId »](mongodb-driver-monitoring-commandstartedevent.getrequestid.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent](class.mongodb-driver-monitoring-commandstartedevent.html)
    
-   Повертає ідентифікатор операції команди
    

# MongoDBDriverMonitoringCommandStartedEvent::getOperationId

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandStartedEvent::getOperationId — Повертає ідентифікатор операції команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandStartedEvent::getOperationId(): string
```

Ідентифікатор операції генерується драйвером і може бути використаний для зв'язування подій разом, таких як операцій масового запису, які можуть бути розділені на кілька команд на рівні протоколу.

> **Зауваження**: Оскільки кілька команд можуть спільно використовувати той самий ідентифікатор операції, недоцільно використовувати його для зв'язування об'єктів подій один з одним. Натомість слід використовувати ідентифікатор запиту, повернутий [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getRequestId()](mongodb-driver-monitoring-commandstartedevent.getrequestid.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор операції команди.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getOperationId()](mongodb-driver-monitoring-commandfailedevent.getoperationid.html) - Повертає ідентифікатор операції команди
-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getOperationId()](mongodb-driver-monitoring-commandsucceededevent.getoperationid.html) - Повертає ідентифікатор операції команди
-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getRequestId()](mongodb-driver-monitoring-commandstartedevent.getrequestid.html) - Повертає ідентифікатор запиту команди
-   [Мониторинг производительности приложения (Application Performance Monitoring или APM)](mongodb.tutorial.apm.html)