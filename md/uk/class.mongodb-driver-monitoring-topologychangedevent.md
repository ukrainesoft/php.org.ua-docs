---
navigation:
  - mongodb-driver-monitoring-serverheartbeatsucceededevent.isawaited.md: '« MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::isAwaited'
  - mongodb-driver-monitoring-topologychangedevent.getnewdescription.md: 'MongoDB\\Driver\\Monitoring\\TopologyChangedEvent::getNewDescription »'
  - index.md: PHP Manual
  - mongodb.monitoring.md: MongoDB\\Driver\\Monitoring
title: Клас MongoDB\\Driver\\Monitoring\\TopologyChangedEvent
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\Driver\\Monitoring\\TopologyChangedEvent

(mongodb >=1.13.0)

## Вступ

Класс**MongoDB\\Driver\\Monitoring\\TopologyChangedEvent** інкапсулює інформацію про змінений опис топології.

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

-   [MongoDB\\Driver\\Monitoring\\TopologyChangedEvent::getNewDescription](mongodb-driver-monitoring-topologychangedevent.getnewdescription.md)— Повертає новий опис топології
-   [MongoDB\\Driver\\Monitoring\\TopologyChangedEvent::getPreviousDescription](mongodb-driver-monitoring-topologychangedevent.getpreviousdescription.md)— Повертає попередній опис топології
-   [MongoDB\\Driver\\Monitoring\\TopologyChangedEvent::getTopologyId](mongodb-driver-monitoring-topologychangedevent.gettopologyid.md) \- Повертає ідентифікатор топології
