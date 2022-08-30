Клас MongoDBDriverMonitoringTopologyChangedEvent

-   [« MongoDBDriverMonitoringServerHeartbeatSucceededEvent::isAwaited](mongodb-driver-monitoring-serverheartbeatsucceededevent.isawaited.html)
    
-   [MongoDBDriverMonitoringTopologyChangedEvent::getNewDescription »](mongodb-driver-monitoring-topologychangedevent.getnewdescription.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverMonitoring](mongodb.monitoring.html)
    
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

-   [MongoDBDriverMonitoringTopologyChangedEvent::getNewDescription](mongodb-driver-monitoring-topologychangedevent.getnewdescription.html) — Повертає новий опис топології
-   [MongoDBDriverMonitoringTopologyChangedEvent::getPreviousDescription](mongodb-driver-monitoring-topologychangedevent.getpreviousdescription.html) — Повертає попередній опис топології
-   [MongoDBDriverMonitoringTopologyChangedEvent::getTopologyId](mongodb-driver-monitoring-topologychangedevent.gettopologyid.html) - Повертає ідентифікатор топології