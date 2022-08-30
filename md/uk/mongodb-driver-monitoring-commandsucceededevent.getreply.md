Повертає документ відповіді команди

-   [« MongoDBDriverMonitoringCommandSucceededEvent::getOperationId](mongodb-driver-monitoring-commandsucceededevent.getoperationid.html)
    
-   [MongoDBDriverMonitoringCommandSucceededEvent::getRequestId »](mongodb-driver-monitoring-commandsucceededevent.getrequestid.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverMonitoringCommandSucceededEvent](class.mongodb-driver-monitoring-commandsucceededevent.html)
    
-   Повертає документ відповіді команди
    

# MongoDBDriverMonitoringCommandSucceededEvent::getReply

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandSucceededEvent::getReply — Повертає документ відповіді команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandSucceededEvent::getReply(): object
```

Документ відповіді буде перетворено з BSON на PHP з використанням правил [десериализации](mongodb.persistence.deserialization.html) (наприклад, документи BSON будуть перетворені на stdClass).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає документ відповіді команди у вигляді об'єкту **stdClass**

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.html)
-   [Постійні дані](mongodb.persistence.html)