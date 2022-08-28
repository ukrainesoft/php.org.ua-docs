Повертає ім'я сервера хоста

-   [« MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::getDurationMicros](mongodb-driver-monitoring-serverheartbeatsucceededevent.getdurationmicros.html)
    
-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::getPort »](mongodb-driver-monitoring-serverheartbeatsucceededevent.getport.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent](class.mongodb-driver-monitoring-serverheartbeatsucceededevent.html)
    
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

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)