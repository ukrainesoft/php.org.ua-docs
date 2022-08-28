Повертає ідентифікатор топології, пов'язаний із цим сервером

-   [« MongoDB\\Driver\\Monitoring\\ServerClosedEvent::getPort](mongodb-driver-monitoring-serverclosedevent.getport.html)
    
-   [MongoDB\\Driver\\Monitoring\\ServerOpeningEvent »](class.mongodb-driver-monitoring-serveropeningevent.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\ServerClosedEvent](class.mongodb-driver-monitoring-serverclosedevent.html)
    
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

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)