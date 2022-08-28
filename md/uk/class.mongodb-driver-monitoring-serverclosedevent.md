Клас MongoDBDriverMonitoringServerClosedEvent

-   [« MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getTopologyId](mongodb-driver-monitoring-serverchangedevent.gettopologyid.html)
    
-   [MongoDB\\Driver\\Monitoring\\ServerClosedEvent::getHost »](mongodb-driver-monitoring-serverclosedevent.gethost.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring](mongodb.monitoring.html)
    
-   Клас MongoDBDriverMonitoringServerClosedEvent
    

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

-   [MongoDB\\Driver\\Monitoring\\ServerClosedEvent::getHost](mongodb-driver-monitoring-serverclosedevent.gethost.html) — Повертає ім'я сервера.
-   [MongoDB\\Driver\\Monitoring\\ServerClosedEvent::getPort](mongodb-driver-monitoring-serverclosedevent.getport.html) — Повертає порт, на якому прослуховується сервер
-   [MongoDB\\Driver\\Monitoring\\ServerClosedEvent::getTopologyId](mongodb-driver-monitoring-serverclosedevent.gettopologyid.html) — Повертає ідентифікатор топології, пов'язаний із цим сервером