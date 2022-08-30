Повертає ім'я сервера хоста

-   [« MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getDurationMicros](mongodb-driver-monitoring-serverheartbeatsucceededevent.getdurationmicros.html)
    
-   [MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getPort »](mongodb-driver-monitoring-serverheartbeatsucceededevent.getport.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverMonitoringServerHeartbeatSucceededEvent](class.mongodb-driver-monitoring-serverheartbeatsucceededevent.html)
    
-   Повертає ім'я сервера хоста
    

# MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getHost

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getHost — Повертає ім'я сервера.

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerHeartbeatSucceededEvent::getHost(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я сервера хоста.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)