Повертає ідентифікатор топології

-   [« MongoDBDriverMonitoringTopologyChangedEvent::getPreviousDescription](mongodb-driver-monitoring-topologychangedevent.getpreviousdescription.html)
    
-   [MongoDBDriverMonitoringTopologyClosedEvent »](class.mongodb-driver-monitoring-topologyclosedevent.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverMonitoringTopologyChangedEvent](class.mongodb-driver-monitoring-topologychangedevent.html)
    
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

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)