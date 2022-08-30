Клас MongoDBDriverMonitoringServerOpeningEvent

-   [« MongoDBDriverMonitoringServerClosedEvent::getTopologyId](mongodb-driver-monitoring-serverclosedevent.gettopologyid.html)
    
-   [MongoDBDriverMonitoringServerOpeningEvent::getHost »](mongodb-driver-monitoring-serveropeningevent.gethost.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverMonitoring](mongodb.monitoring.html)
    
-   Клас MongoDBDriverMonitoringServerOpeningEvent
    

# Клас MongoDBDriverMonitoringServerOpeningEvent

(mongodb >=1.13.0)

## Вступ

Клас **MongoDBDriverMonitoringServerOpeningEvent** інкапсулює інформацію про відкритий сервер.

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

-   [MongoDBDriverMonitoringServerOpeningEvent::getHost](mongodb-driver-monitoring-serveropeningevent.gethost.html) — Повертає ім'я сервера.
-   [MongoDBDriverMonitoringServerOpeningEvent::getPort](mongodb-driver-monitoring-serveropeningevent.getport.html) — Повертає порт, на якому прослуховується сервер
-   [MongoDBDriverMonitoringServerOpeningEvent::getTopologyId](mongodb-driver-monitoring-serveropeningevent.gettopologyid.html) — Returns the topology ID associated with this server