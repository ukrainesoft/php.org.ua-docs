Повертає документ відповіді команди

-   [« MongoDBDriverMonitoringCommandFailedEvent::getOperationId](mongodb-driver-monitoring-commandfailedevent.getoperationid.html)
    
-   [MongoDBDriverMonitoringCommandFailedEvent::getRequestId »](mongodb-driver-monitoring-commandfailedevent.getrequestid.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverMonitoringCommandFailedEvent](class.mongodb-driver-monitoring-commandfailedevent.html)
    
-   Повертає документ відповіді команди
    

# MongoDBDriverMonitoringCommandFailedEvent::getReply

(mongodb >=1.5.0)

MongoDBDriverMonitoringCommandFailedEvent::getReply — Повертає документ відповіді команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\CommandFailedEvent::getReply(): object
```

У відповідь документ буде перетворено з BSON в PHP з використанням правил [десериализации](mongodb.persistence.deserialization.html) за промовчанням (наприклад, документи BSON будуть перетворені на stdClass).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає документ відповіді команди у вигляді об'єкту **stdClass**

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.html)
-   [Постійні дані](mongodb.persistence.html)