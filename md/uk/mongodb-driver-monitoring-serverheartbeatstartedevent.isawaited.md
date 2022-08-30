Повертає, чи використовувався в heartbeat потоковий протокол

-   [« MongoDBDriverMonitoringServerHeartbeatStartedEvent::getPort](mongodb-driver-monitoring-serverheartbeatstartedevent.getport.html)
    
-   [MongoDBDriverMonitoringServerHeartbeatSucceededEvent »](class.mongodb-driver-monitoring-serverheartbeatsucceededevent.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverMonitoringServerHeartbeatStartedEvent](class.mongodb-driver-monitoring-serverheartbeatstartedevent.html)
    
-   Повертає, чи використовувався в heartbeat потоковий протокол
    

# MongoDBDriverMonitoringServerHeartbeatStartedEvent::isAwaited

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerHeartbeatStartedEvent::isAwaited — Повертає, чи використовувався в heartbeat потоковий протокол

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerHeartbeatStartedEvent::isAwaited(): bool
```

Повертає, чи використовувався в heartbeat потоковий протокол. Драйвер PHP не використовує потоковий протокол для моніторингу, тому цей метод завжди повертатиметься **`false`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`false`**

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)