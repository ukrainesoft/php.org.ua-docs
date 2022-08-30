Повертає ідентифікатор топології, пов'язаний із цим сервером

-   [« MongoDBDriverMonitoringServerChangedEvent::getPreviousDescription](mongodb-driver-monitoring-serverchangedevent.getpreviousdescription.html)
    
-   [MongoDBDriverMonitoringServerClosedEvent »](class.mongodb-driver-monitoring-serverclosedevent.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverMonitoringServerChangedEvent](class.mongodb-driver-monitoring-serverchangedevent.html)
    
-   Повертає ідентифікатор топології, пов'язаний із цим сервером
    

# MongoDBDriverMonitoringServerChangedEvent::getTopologyId

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerChangedEvent::getTopologyId — Повертає ідентифікатор топології, пов'язаний із цим сервером

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerChangedEvent::getTopologyId(): MongoDB\BSON\ObjectId
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор топології.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)