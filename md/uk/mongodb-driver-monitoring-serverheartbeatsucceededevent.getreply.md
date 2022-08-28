Повертає документ відповіді heartbeat

-   [« MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::getPort](mongodb-driver-monitoring-serverheartbeatsucceededevent.getport.html)
    
-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::isAwaited »](mongodb-driver-monitoring-serverheartbeatsucceededevent.isawaited.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent](class.mongodb-driver-monitoring-serverheartbeatsucceededevent.html)
    
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

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [Мониторинг производительности приложения (Application Performance Monitoring или APM)](mongodb.tutorial.apm.html)
-   [Постоянные данные](mongodb.persistence.html)