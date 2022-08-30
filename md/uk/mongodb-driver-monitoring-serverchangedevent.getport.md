Повертає порт, на якому прослуховується сервер

-   [« MongoDBDriverMonitoringServerChangedEvent::getNewDescription](mongodb-driver-monitoring-serverchangedevent.getnewdescription.html)
    
-   [MongoDBDriverMonitoringServerChangedEvent::getPreviousDescription »](mongodb-driver-monitoring-serverchangedevent.getpreviousdescription.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverMonitoringServerChangedEvent](class.mongodb-driver-monitoring-serverchangedevent.html)
    
-   Повертає порт, на якому прослуховується сервер
    

# MongoDBDriverMonitoringServerChangedEvent::getPort

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerChangedEvent::getPort — Повертає порт, на якому прослуховується сервер

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerChangedEvent::getPort(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає порт, у якому прослуховується сервер.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)