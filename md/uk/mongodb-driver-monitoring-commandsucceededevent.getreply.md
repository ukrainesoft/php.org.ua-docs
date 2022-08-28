Повертає документ відповіді команди

-   [« MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getOperationId](mongodb-driver-monitoring-commandsucceededevent.getoperationid.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getRequestId »](mongodb-driver-monitoring-commandsucceededevent.getrequestid.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent](class.mongodb-driver-monitoring-commandsucceededevent.html)
    
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

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [Мониторинг производительности приложения (Application Performance Monitoring или APM)](mongodb.tutorial.apm.html)
-   [Постоянные данные](mongodb.persistence.html)