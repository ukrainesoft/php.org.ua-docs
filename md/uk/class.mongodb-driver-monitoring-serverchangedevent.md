Клас MongoDBDriverMonitoringServerChangedEvent

-   [« MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getServiceId](mongodb-driver-monitoring-commandsucceededevent.getserviceid.html)
    
-   [MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getHost »](mongodb-driver-monitoring-serverchangedevent.gethost.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring](mongodb.monitoring.html)
    
-   Клас MongoDBDriverMonitoringServerChangedEvent
    

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

-   [MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getHost](mongodb-driver-monitoring-serverchangedevent.gethost.html) — Повертає ім'я сервера.
-   [MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getNewDescription](mongodb-driver-monitoring-serverchangedevent.getnewdescription.html) — Повертає новий опис сервера
-   [MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getPort](mongodb-driver-monitoring-serverchangedevent.getport.html) — Повертає порт, на якому прослуховується сервер
-   [MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getPreviousDescription](mongodb-driver-monitoring-serverchangedevent.getpreviousdescription.html) — Повертає попередній опис сервера
-   [MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getTopologyId](mongodb-driver-monitoring-serverchangedevent.gettopologyid.html) — Повертає ідентифікатор топології, пов'язаний із цим сервером