Повертає ідентифікатор топології, пов'язаний із цим сервером

-   [« MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getPreviousDescription](mongodb-driver-monitoring-serverchangedevent.getpreviousdescription.html)
    
-   [MongoDB\\Driver\\Monitoring\\ServerClosedEvent »](class.mongodb-driver-monitoring-serverclosedevent.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\ServerChangedEvent](class.mongodb-driver-monitoring-serverchangedevent.html)
    
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

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)