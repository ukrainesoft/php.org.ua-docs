---
navigation:
  - mongodb-driver-monitoring-serverclosedevent.gettopologyid.md: '« MongoDB\\Driver\\Monitoring\\ServerClosedEvent::getTopologyId'
  - mongodb-driver-monitoring-serveropeningevent.gethost.md: 'MongoDB\\Driver\\Monitoring\\ServerOpeningEvent::getHost »'
  - index.md: PHP Manual
  - mongodb.monitoring.md: MongoDB\\Driver\\Monitoring
title: Клас MongoDB\\Driver\\Monitoring\\ServerOpeningEvent
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\Driver\\Monitoring\\ServerOpeningEvent

(mongodb >=1.13.0)

## Вступ

Класс**MongoDB\\Driver\\Monitoring\\ServerOpeningEvent** інкапсулює інформацію про відкритий сервер.

## Огляд класів

```classsynopsis


    
    
     final
     
      class MongoDB\Driver\Monitoring\ServerOpeningEvent
     
     {
    

    /* Методы */
    
   final public getHost(): string
final public getPort(): int
final public getTopologyId(): MongoDB\BSON\ObjectId

   }
```

## Зміст

-   [MongoDB\\Driver\\Monitoring\\ServerOpeningEvent::getHost](mongodb-driver-monitoring-serveropeningevent.gethost.md)— Повертає ім'я сервера.
-   [MongoDB\\Driver\\Monitoring\\ServerOpeningEvent::getPort](mongodb-driver-monitoring-serveropeningevent.getport.md)— Повертає порт, на якому прослуховується сервер
-   [MongoDB\\Driver\\Monitoring\\ServerOpeningEvent::getTopologyId](mongodb-driver-monitoring-serveropeningevent.gettopologyid.md)— Returns the topology ID associated with this server
