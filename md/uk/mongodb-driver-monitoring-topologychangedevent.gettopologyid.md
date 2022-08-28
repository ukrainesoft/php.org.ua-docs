Повертає ідентифікатор топології

-   [« MongoDB\\Driver\\Monitoring\\TopologyChangedEvent::getPreviousDescription](mongodb-driver-monitoring-topologychangedevent.getpreviousdescription.html)
    
-   [MongoDB\\Driver\\Monitoring\\TopologyClosedEvent »](class.mongodb-driver-monitoring-topologyclosedevent.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\TopologyChangedEvent](class.mongodb-driver-monitoring-topologychangedevent.html)
    
-   Повертає ідентифікатор топології
    

# MongoDBDriverMonitoringTopologyChangedEvent::getTopologyId

(mongodb >=1.13.0)

MongoDBDriverMonitoringTopologyChangedEvent::getTopologyId — Повертає ідентифікатор топології

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\TopologyChangedEvent::getTopologyId(): MongoDB\BSON\ObjectId
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор топології.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)