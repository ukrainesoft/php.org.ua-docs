Повертає тривалість heartbeat у мікросекундах

-   [« MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent](class.mongodb-driver-monitoring-serverheartbeatfailedevent.html)
    
-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::getError »](mongodb-driver-monitoring-serverheartbeatfailedevent.geterror.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent](class.mongodb-driver-monitoring-serverheartbeatfailedevent.html)
    
-   Повертає тривалість heartbeat у мікросекундах
    

# MongoDBDriverMonitoringServerHeartbeatFailedEvent::getDurationMicros

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerHeartbeatFailedEvent::getDurationMicros — Повертає тривалість heartbeat у мікросекундах

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerHeartbeatFailedEvent::getDurationMicros(): int
```

Тривалість heartbeat - це розрахункове значення, яке включає час відправки повідомлення і отримання відповіді від сервера.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає тривалість heartbeat в мікросекундах.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)