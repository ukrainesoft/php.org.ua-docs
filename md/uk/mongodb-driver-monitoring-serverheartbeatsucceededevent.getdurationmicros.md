Повертає тривалість heartbeat у мікросекундах

-   [« MongoDBDriverMonitoringServerHeartbeatSucceededEvent](class.mongodb-driver-monitoring-serverheartbeatsucceededevent.html)
    
-   [MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getHost »](mongodb-driver-monitoring-serverheartbeatsucceededevent.gethost.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverMonitoringServerHeartbeatSucceededEvent](class.mongodb-driver-monitoring-serverheartbeatsucceededevent.html)
    
-   Повертає тривалість heartbeat у мікросекундах
    

# MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getDurationMicros

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getDurationMicros — Повертає тривалість heartbeat у мікросекундах

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerHeartbeatSucceededEvent::getDurationMicros(): int
```

Тривалість heartbeat - це розрахункове значення, яке включає час відправки повідомлення і отримання відповіді від сервера.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає тривалість heartbeat в мікросекундах.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)