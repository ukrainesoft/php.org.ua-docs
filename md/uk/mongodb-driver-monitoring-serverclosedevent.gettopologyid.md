Повертає ідентифікатор топології, пов'язаний із цим сервером

-   [« MongoDBDriverMonitoringServerClosedEvent::getPort](mongodb-driver-monitoring-serverclosedevent.getport.html)
    
-   [MongoDBDriverMonitoringServerOpeningEvent »](class.mongodb-driver-monitoring-serveropeningevent.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverMonitoringServerClosedEvent](class.mongodb-driver-monitoring-serverclosedevent.html)
    
-   Повертає ідентифікатор топології, пов'язаний із цим сервером
    

# MongoDBDriverMonitoringServerClosedEvent::getTopologyId

(mongodb >=1.13.0)

MongoDBDriverMonitoringServerClosedEvent::getTopologyId — Повертає ідентифікатор топології, пов'язаний із цим сервером

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\ServerClosedEvent::getTopologyId(): MongoDB\BSON\ObjectId
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор топології.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)