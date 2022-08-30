Повертає, чи використовувався в heartbeat потоковий протокол

-   [« MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getReply](mongodb-driver-monitoring-serverheartbeatsucceededevent.getreply.html)
    
-   [MongoDBDriverMonitoringTopologyChangedEvent »](class.mongodb-driver-monitoring-topologychangedevent.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverMonitoringServerHeartbeatSucceededEvent](class.mongodb-driver-monitoring-serverheartbeatsucceededevent.html)
    
-   Повертає, чи використовувався в heartbeat потоковий протокол
    

# MongoDBDriverMonitoringServerHeartbeatSucceededEvent::isAwaited

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerHeartbeatSucceededEvent::isAwaited — Повертає, чи використовувався в heartbeat потоковий протокол

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerHeartbeatSucceededEvent::isAwaited(): bool
```

Повертає, чи використовувався в heartbeat потоковий протокол. Драйвер PHP не використовує потоковий протокол для моніторингу, тому цей метод завжди повертатиметься **`false`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`false`**

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)