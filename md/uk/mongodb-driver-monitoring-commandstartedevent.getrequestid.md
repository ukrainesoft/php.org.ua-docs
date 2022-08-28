Повертає ідентифікатор запиту команди

-   [« MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getOperationId](mongodb-driver-monitoring-commandstartedevent.getoperationid.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getServer »](mongodb-driver-monitoring-commandstartedevent.getserver.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent](class.mongodb-driver-monitoring-commandstartedevent.html)
    
-   Повертає ідентифікатор запиту команди
    

# MongoDBDriverMonitoringCommandStartedEvent::getRequestId

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandStartedEvent::getRequestId — Повертає ідентифікатор запиту команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandStartedEvent::getRequestId(): string
```

Ідентифікатор запиту генерується драйвером і може бути використаний для зв'язування [MongoDB\\Driver\\Monitoring\\CommandStartedEvent](class.mongodb-driver-monitoring-commandstartedevent.html) з наступним [MongoDB\\Driver\\Monitoring\\CommandFailedEvent](class.mongodb-driver-monitoring-commandfailedevent.html) або [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent](class.mongodb-driver-monitoring-commandsucceededevent.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор запиту команди.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getRequestId()](mongodb-driver-monitoring-commandfailedevent.getrequestid.html) - Повертає ідентифікатор запиту команди
-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getRequestId()](mongodb-driver-monitoring-commandsucceededevent.getrequestid.html) - Повертає ідентифікатор запиту команди
-   [Мониторинг производительности приложения (Application Performance Monitoring или APM)](mongodb.tutorial.apm.html)