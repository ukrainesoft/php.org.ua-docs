Повертає порт, на якому прослуховується сервер

-   [« MongoDBDriverMonitoringServerHeartbeatFailedEvent::getHost](mongodb-driver-monitoring-serverheartbeatfailedevent.gethost.html)
    
-   [MongoDBDriverMonitoringServerHeartbeatFailedEvent::isAwaited »](mongodb-driver-monitoring-serverheartbeatfailedevent.isawaited.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverMonitoringServerHeartbeatFailedEvent](class.mongodb-driver-monitoring-serverheartbeatfailedevent.html)
    
-   Повертає порт, на якому прослуховується сервер
    

# MongoDBDriverMonitoringServerHeartbeatFailedEvent::getPort

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerHeartbeatFailedEvent::getPort — Повертає порт, на якому прослуховується сервер

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerHeartbeatFailedEvent::getPort(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає порт, у якому прослуховується сервер.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)