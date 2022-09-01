---
navigation:
  - mongodb-driver-monitoring-serverchangedevent.gettopologyid.html: '« MongoDBDriverMonitoringServerChangedEvent::getTopologyId'
  - mongodb-driver-monitoring-serverclosedevent.gethost.html: 'MongoDBDriverMonitoringServerClosedEvent::getHost »'
  - index.md: PHP Manual
  - mongodb.monitoring.md: MongoDBDriverMonitoring
title: Клас MongoDBDriverMonitoringServerClosedEvent
---
# Клас MongoDBDriverMonitoringServerClosedEvent

(mongodb >=1.13.0)

## Вступ

Клас **MongoDBDriverMonitoringServerClosedEvent** інкапсулює інформацію про закритий сервер.

## Огляд класів

```classsynopsis


    
    
     final
     
      class MongoDB\Driver\Monitoring\ServerClosedEvent
     
     {
    

    /* Методы */
    
   final public getHost(): string
final public getPort(): int
final public getTopologyId(): MongoDB\BSON\ObjectId

   }
```

## Зміст

-   [MongoDBDriverMonitoringServerClosedEvent::getHost](mongodb-driver-monitoring-serverclosedevent.gethost.md) — Повертає ім'я сервера.
-   [MongoDBDriverMonitoringServerClosedEvent::getPort](mongodb-driver-monitoring-serverclosedevent.getport.md) — Повертає порт, на якому прослуховується сервер
-   [MongoDBDriverMonitoringServerClosedEvent::getTopologyId](mongodb-driver-monitoring-serverclosedevent.gettopologyid.md) — Повертає ідентифікатор топології, пов'язаний із цим сервером
