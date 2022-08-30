Повертає ім'я сервера хоста

-   [« MongoDBDriverMonitoringServerHeartbeatStartedEvent](class.mongodb-driver-monitoring-serverheartbeatstartedevent.html)
    
-   [MongoDBDriverMonitoringServerHeartbeatStartedEvent::getPort »](mongodb-driver-monitoring-serverheartbeatstartedevent.getport.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverMonitoringServerHeartbeatStartedEvent](class.mongodb-driver-monitoring-serverheartbeatstartedevent.html)
    
-   Повертає ім'я сервера хоста
    

# MongoDBDriverMonitoringServerHeartbeatStartedEvent::getHost

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerHeartbeatStartedEvent::getHost — Повертає ім'я сервера.

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerHeartbeatStartedEvent::getHost(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я сервера хоста.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)