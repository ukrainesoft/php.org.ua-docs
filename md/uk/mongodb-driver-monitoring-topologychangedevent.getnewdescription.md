Повертає новий опис топології

-   [« MongoDB\\Driver\\Monitoring\\TopologyChangedEvent](class.mongodb-driver-monitoring-topologychangedevent.html)
    
-   [MongoDB\\Driver\\Monitoring\\TopologyChangedEvent::getPreviousDescription »](mongodb-driver-monitoring-topologychangedevent.getpreviousdescription.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\TopologyChangedEvent](class.mongodb-driver-monitoring-topologychangedevent.html)
    
-   Повертає новий опис топології
    

# MongoDBDriverMonitoringTopologyChangedEvent::getNewDescription

(mongodb >=1.13.0)

MongoDBDriverMonitoringTopologyChangedEvent::getNewDescription — Повертає новий опис топології

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\TopologyChangedEvent::getNewDescription(): MongoDB\Driver\TopologyDescription
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає новий опис ([MongoDB\\Driver\\TopologyDescription](class.mongodb-driver-topologydescription.html)) топології.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)