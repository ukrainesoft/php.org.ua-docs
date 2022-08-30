Повертає порт, на якому прослуховується сервер

-   [« MongoDBDriverMonitoringServerHeartbeatStartedEvent::getHost](mongodb-driver-monitoring-serverheartbeatstartedevent.gethost.html)
    
-   [MongoDBDriverMonitoringServerHeartbeatStartedEvent::isAwaited »](mongodb-driver-monitoring-serverheartbeatstartedevent.isawaited.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverMonitoringServerHeartbeatStartedEvent](class.mongodb-driver-monitoring-serverheartbeatstartedevent.html)
    
-   Повертає порт, на якому прослуховується сервер
    

# MongoDBDriverMonitoringServerHeartbeatStartedEvent::getPort

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerHeartbeatStartedEvent::getPort — Повертає порт, на якому прослуховується сервер

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerHeartbeatStartedEvent::getPort(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає порт, у якому прослуховується сервер.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)