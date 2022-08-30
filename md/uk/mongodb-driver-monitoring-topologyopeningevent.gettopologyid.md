Повертає ідентифікатор топології

-   [« MongoDBDriverMonitoringTopologyOpeningEvent](class.mongodb-driver-monitoring-topologyopeningevent.html)
    
-   [MongoDBDriverMonitoringCommandSubscriber »](class.mongodb-driver-monitoring-commandsubscriber.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverMonitoringTopologyOpeningEvent](class.mongodb-driver-monitoring-topologyopeningevent.html)
    
-   Повертає ідентифікатор топології
    

# MongoDBDriverMonitoringTopologyOpeningEvent::getTopologyId

(mongodb >=1.13.0)

MongoDBDriverMonitoringTopologyOpeningEvent::getTopologyId — Повертає ідентифікатор топології

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\TopologyOpeningEvent::getTopologyId(): MongoDB\BSON\ObjectId
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор топології.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)