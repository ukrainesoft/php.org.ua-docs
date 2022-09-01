---
navigation:
  - mongodb-driver-monitoring-commandsucceededevent.getserviceid.html: '« MongoDBDriverMonitoringCommandSucceededEvent::getServiceId'
  - mongodb-driver-monitoring-serverchangedevent.gethost.html: 'MongoDBDriverMonitoringServerChangedEvent::getHost »'
  - index.md: PHP Manual
  - mongodb.monitoring.md: MongoDBDriverMonitoring
title: Клас MongoDBDriverMonitoringServerChangedEvent
---
# Клас MongoDBDriverMonitoringServerChangedEvent

(mongodb >=1.13.0)

## Вступ

Клас **MongoDBDriverMonitoringServerChangedEvent** інкапсулює інформацію про зміну опису сервера.

## Огляд класів

```classsynopsis


    
    
     final
     
      class MongoDB\Driver\Monitoring\ServerChangedEvent
     
     {
    

    /* Методы */
    
   final public getHost(): string
final public getNewDescription(): MongoDB\Driver\ServerDescription
final public getPort(): int
final public getPreviousDescription(): MongoDB\Driver\ServerDescription
final public getTopologyId(): MongoDB\BSON\ObjectId

   }
```

## Зміст

-   [MongoDBDriverMonitoringServerChangedEvent::getHost](mongodb-driver-monitoring-serverchangedevent.gethost.md) — Повертає ім'я сервера.
-   [MongoDBDriverMonitoringServerChangedEvent::getNewDescription](mongodb-driver-monitoring-serverchangedevent.getnewdescription.md) — Повертає новий опис сервера
-   [MongoDBDriverMonitoringServerChangedEvent::getPort](mongodb-driver-monitoring-serverchangedevent.getport.md) — Повертає порт, на якому прослуховується сервер
-   [MongoDBDriverMonitoringServerChangedEvent::getPreviousDescription](mongodb-driver-monitoring-serverchangedevent.getpreviousdescription.md) — Повертає попередній опис сервера
-   [MongoDBDriverMonitoringServerChangedEvent::getTopologyId](mongodb-driver-monitoring-serverchangedevent.gettopologyid.md) — Повертає ідентифікатор топології, пов'язаний із цим сервером
