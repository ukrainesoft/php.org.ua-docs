Повертає ідентифікатор запиту команди

-   [« MongoDBDriverMonitoringCommandFailedEvent::getReply](mongodb-driver-monitoring-commandfailedevent.getreply.html)
    
-   [MongoDBDriverMonitoringCommandFailedEvent::getServer »](mongodb-driver-monitoring-commandfailedevent.getserver.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverMonitoringCommandFailedEvent](class.mongodb-driver-monitoring-commandfailedevent.html)
    
-   Повертає ідентифікатор запиту команди
    

# MongoDBDriverMonitoringCommandFailedEvent::getRequestId

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandFailedEvent::getRequestId — Повертає ідентифікатор запиту команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandFailedEvent::getRequestId(): string
```

Ідентифікатор запиту генерується драйвером і може бути використаний для зв'язування [MongoDBDriverMonitoringCommandFailedEvent](class.mongodb-driver-monitoring-commandfailedevent.html) з попереднім [MongoDBDriverMonitoringCommandStartedEvent](class.mongodb-driver-monitoring-commandstartedevent.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор запиту команди.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverMonitoringCommandStartedEvent::getRequestId()](mongodb-driver-monitoring-commandstartedevent.getrequestid.html) - Повертає ідентифікатор запиту команди
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)