Повертає документ відповіді heartbeat

-   [« MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getPort](mongodb-driver-monitoring-serverheartbeatsucceededevent.getport.html)
    
-   [MongoDBDriverMonitoringServerHeartbeatSucceededEvent::isAwaited »](mongodb-driver-monitoring-serverheartbeatsucceededevent.isawaited.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverMonitoringServerHeartbeatSucceededEvent](class.mongodb-driver-monitoring-serverheartbeatsucceededevent.html)
    
-   Повертає документ відповіді heartbeat
    

# MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getReply

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getReply — Повертає документ відповіді heartbeat

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerHeartbeatSucceededEvent::getReply(): object
```

Документ відповіді буде перетворено з BSON на PHP з використанням правил [десериализации](mongodb.persistence.deserialization.html) за промовчанням (наприклад, документи BSON будуть перетворені на stdClass).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає документ відповіді heartbeat у вигляді об'єкта **stdClass**

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.html)
-   [Постійні дані](mongodb.persistence.html)