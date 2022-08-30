Повертає ім'я сервера хоста

-   [« MongoDBDriverMonitoringServerHeartbeatFailedEvent::getError](mongodb-driver-monitoring-serverheartbeatfailedevent.geterror.html)
    
-   [MongoDBDriverMonitoringServerHeartbeatFailedEvent::getPort »](mongodb-driver-monitoring-serverheartbeatfailedevent.getport.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverMonitoringServerHeartbeatFailedEvent](class.mongodb-driver-monitoring-serverheartbeatfailedevent.html)
    
-   Повертає ім'я сервера хоста
    

# MongoDBDriverMonitoringServerHeartbeatFailedEvent::getHost

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerHeartbeatFailedEvent::getHost — Повертає ім'я сервера.

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerHeartbeatFailedEvent::getHost(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я сервера хоста.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)