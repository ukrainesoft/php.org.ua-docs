Клас MongoDBDriverMonitoringServerClosedEvent

-   [« MongoDBDriverMonitoringServerChangedEvent::getTopologyId](mongodb-driver-monitoring-serverchangedevent.gettopologyid.html)
    
-   [MongoDBDriverMonitoringServerClosedEvent::getHost »](mongodb-driver-monitoring-serverclosedevent.gethost.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverMonitoring](mongodb.monitoring.html)
    
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

-   [MongoDBDriverMonitoringServerClosedEvent::getHost](mongodb-driver-monitoring-serverclosedevent.gethost.html) — Повертає ім'я сервера.
-   [MongoDBDriverMonitoringServerClosedEvent::getPort](mongodb-driver-monitoring-serverclosedevent.getport.html) — Повертає порт, на якому прослуховується сервер
-   [MongoDBDriverMonitoringServerClosedEvent::getTopologyId](mongodb-driver-monitoring-serverclosedevent.gettopologyid.html) — Повертає ідентифікатор топології, пов'язаний із цим сервером