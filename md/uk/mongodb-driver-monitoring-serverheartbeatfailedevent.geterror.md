Повертає виняток, пов'язаний з невдалим виконанням heartbeat

-   [« MongoDBDriverMonitoringServerHeartbeatFailedEvent::getDurationMicros](mongodb-driver-monitoring-serverheartbeatfailedevent.getdurationmicros.html)
    
-   [MongoDBDriverMonitoringServerHeartbeatFailedEvent::getHost »](mongodb-driver-monitoring-serverheartbeatfailedevent.gethost.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverMonitoringServerHeartbeatFailedEvent](class.mongodb-driver-monitoring-serverheartbeatfailedevent.html)
    
-   Повертає виняток, пов'язаний з невдалим виконанням heartbeat
    

# MongoDBDriverMonitoringServerHeartbeatFailedEvent::getError

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerHeartbeatFailedEvent::getError — Повертає виняток, пов'язаний із невдалим виконанням heartbeat

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerHeartbeatFailedEvent::getError(): Exception
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає виняток ([Exception](class.exception.html)), пов'язане з невдалим виконанням heartbeat.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)