Повертає ідентифікатор запиту команди

-   [« MongoDBDriverMonitoringCommandSucceededEvent::getReply](mongodb-driver-monitoring-commandsucceededevent.getreply.html)
    
-   [MongoDBDriverMonitoringCommandSucceededEvent::getServer »](mongodb-driver-monitoring-commandsucceededevent.getserver.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverMonitoringCommandSucceededEvent](class.mongodb-driver-monitoring-commandsucceededevent.html)
    
-   Повертає ідентифікатор запиту команди
    

# MongoDBDriverMonitoringCommandSucceededEvent::getRequestId

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandSucceededEvent::getRequestId — Повертає ідентифікатор запиту команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandSucceededEvent::getRequestId(): string
```

Ідентифікатор запиту генерується драйвером і може бути використаний для зв'язування [MongoDBDriverMonitoringCommandSucceededEvent](class.mongodb-driver-monitoring-commandsucceededevent.html) з попереднім [MongoDBDriverMonitoringCommandStartedEvent](class.mongodb-driver-monitoring-commandstartedevent.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор запиту команди.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverMonitoringCommandStartedEvent::getRequestId()](mongodb-driver-monitoring-commandstartedevent.getrequestid.html) - Повертає ідентифікатор запиту команди
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.html)