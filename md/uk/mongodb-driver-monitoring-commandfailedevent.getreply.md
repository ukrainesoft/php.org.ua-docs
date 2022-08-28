Повертає документ відповіді команди

-   [« MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getOperationId](mongodb-driver-monitoring-commandfailedevent.getoperationid.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getRequestId »](mongodb-driver-monitoring-commandfailedevent.getrequestid.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent](class.mongodb-driver-monitoring-commandfailedevent.html)
    
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

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [Мониторинг производительности приложения (Application Performance Monitoring или APM)](mongodb.tutorial.apm.html)
-   [Постоянные данные](mongodb.persistence.html)