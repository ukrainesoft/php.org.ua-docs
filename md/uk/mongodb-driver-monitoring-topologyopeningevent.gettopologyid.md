Повертає ідентифікатор топології

-   [« MongoDB\\Driver\\Monitoring\\TopologyOpeningEvent](class.mongodb-driver-monitoring-topologyopeningevent.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandSubscriber »](class.mongodb-driver-monitoring-commandsubscriber.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\TopologyOpeningEvent](class.mongodb-driver-monitoring-topologyopeningevent.html)
    
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

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)