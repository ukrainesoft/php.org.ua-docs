Клас MongoDBDriverMonitoringTopologyChangedEvent

-   [« MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::isAwaited](mongodb-driver-monitoring-serverheartbeatsucceededevent.isawaited.html)
    
-   [MongoDB\\Driver\\Monitoring\\TopologyChangedEvent::getNewDescription »](mongodb-driver-monitoring-topologychangedevent.getnewdescription.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring](mongodb.monitoring.html)
    
-   Клас MongoDBDriverMonitoringTopologyChangedEvent
    

# Клас MongoDBDriverMonitoringTopologyChangedEvent

(mongodb >=1.13.0)

## Вступ

Клас **MongoDBDriverMonitoringTopologyChangedEvent** інкапсулює інформацію про змінений опис топології.

## Огляд класів

```classsynopsis


    
    
     final
     
      class MongoDB\Driver\Monitoring\TopologyChangedEvent
     
     {
    

    /* Методы */
    
   final public getNewDescription(): MongoDB\Driver\TopologyDescription
final public getPreviousDescription(): MongoDB\Driver\TopologyDescription
final public getTopologyId(): MongoDB\BSON\ObjectId

   }
```

## Зміст

-   [MongoDB\\Driver\\Monitoring\\TopologyChangedEvent::getNewDescription](mongodb-driver-monitoring-topologychangedevent.getnewdescription.html) — Повертає новий опис топології
-   [MongoDB\\Driver\\Monitoring\\TopologyChangedEvent::getPreviousDescription](mongodb-driver-monitoring-topologychangedevent.getpreviousdescription.html) — Повертає попередній опис топології
-   [MongoDB\\Driver\\Monitoring\\TopologyChangedEvent::getTopologyId](mongodb-driver-monitoring-topologychangedevent.gettopologyid.html) - Повертає ідентифікатор топології