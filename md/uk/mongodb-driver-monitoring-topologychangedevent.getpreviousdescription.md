Повертає попередній опис топології

-   [« MongoDB\\Driver\\Monitoring\\TopologyChangedEvent::getNewDescription](mongodb-driver-monitoring-topologychangedevent.getnewdescription.html)
    
-   [MongoDB\\Driver\\Monitoring\\TopologyChangedEvent::getTopologyId »](mongodb-driver-monitoring-topologychangedevent.gettopologyid.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\TopologyChangedEvent](class.mongodb-driver-monitoring-topologychangedevent.html)
    
-   Повертає попередній опис топології
    

# MongoDBDriverMonitoringTopology Changed Event::get Previous Description

(mongodb >=1.13.0)

MongoDBDriverMonitoringTopologyChangedEvent::getPreviousDescription — Повертає попередній опис топології

### Опис

```methodsynopsis
final public MongoDB\Driver\Monitoring\TopologyChangedEvent::getPreviousDescription(): MongoDB\Driver\TopologyDescription
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає попередній опис ([MongoDB\\Driver\\TopologyDescription](class.mongodb-driver-topologydescription.html)) топології.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)