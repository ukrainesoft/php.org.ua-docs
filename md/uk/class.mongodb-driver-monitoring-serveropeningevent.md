Клас MongoDBDriverMonitoringServerOpeningEvent

-   [« MongoDB\\Driver\\Monitoring\\ServerClosedEvent::getTopologyId](mongodb-driver-monitoring-serverclosedevent.gettopologyid.html)
    
-   [MongoDB\\Driver\\Monitoring\\ServerOpeningEvent::getHost »](mongodb-driver-monitoring-serveropeningevent.gethost.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring](mongodb.monitoring.html)
    
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

-   [MongoDB\\Driver\\Monitoring\\ServerOpeningEvent::getHost](mongodb-driver-monitoring-serveropeningevent.gethost.html) — Повертає ім'я сервера.
-   [MongoDB\\Driver\\Monitoring\\ServerOpeningEvent::getPort](mongodb-driver-monitoring-serveropeningevent.getport.html) — Повертає порт, на якому прослуховується сервер
-   [MongoDB\\Driver\\Monitoring\\ServerOpeningEvent::getTopologyId](mongodb-driver-monitoring-serveropeningevent.gettopologyid.html) — Returns the topology ID associated with this server