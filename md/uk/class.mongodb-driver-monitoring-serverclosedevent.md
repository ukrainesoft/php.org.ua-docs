---
navigation:
  - mongodb-driver-monitoring-serverchangedevent.gettopologyid.md: '« MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getTopologyId'
  - mongodb-driver-monitoring-serverclosedevent.gethost.md: 'MongoDB\\Driver\\Monitoring\\ServerClosedEvent::getHost »'
  - index.md: PHP Manual
  - mongodb.monitoring.md: MongoDB\\Driver\\Monitoring
title: Клас MongoDB\\Driver\\Monitoring\\ServerClosedEvent
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\Driver\\Monitoring\\ServerClosedEvent

(mongodb >=1.13.0)

## Вступ

Класс**MongoDB\\Driver\\Monitoring\\ServerClosedEvent** інкапсулює інформацію про закритий сервер.

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

-   [MongoDB\\Driver\\Monitoring\\ServerClosedEvent::getHost](mongodb-driver-monitoring-serverclosedevent.gethost.md)— Повертає ім'я сервера.
-   [MongoDB\\Driver\\Monitoring\\ServerClosedEvent::getPort](mongodb-driver-monitoring-serverclosedevent.getport.md)— Повертає порт, на якому прослуховується сервер
-   [MongoDB\\Driver\\Monitoring\\ServerClosedEvent::getTopologyId](mongodb-driver-monitoring-serverclosedevent.gettopologyid.md)— Повертає ідентифікатор топології, пов'язаний із цим сервером
