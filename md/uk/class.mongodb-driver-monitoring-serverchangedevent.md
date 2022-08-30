Клас MongoDBDriverMonitoringServerChangedEvent

-   [« MongoDBDriverMonitoringCommandSucceededEvent::getServiceId](mongodb-driver-monitoring-commandsucceededevent.getserviceid.html)
    
-   [MongoDBDriverMonitoringServerChangedEvent::getHost »](mongodb-driver-monitoring-serverchangedevent.gethost.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverMonitoring](mongodb.monitoring.html)
    
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

-   [MongoDBDriverMonitoringServerChangedEvent::getHost](mongodb-driver-monitoring-serverchangedevent.gethost.html) — Повертає ім'я сервера.
-   [MongoDBDriverMonitoringServerChangedEvent::getNewDescription](mongodb-driver-monitoring-serverchangedevent.getnewdescription.html) — Повертає новий опис сервера
-   [MongoDBDriverMonitoringServerChangedEvent::getPort](mongodb-driver-monitoring-serverchangedevent.getport.html) — Повертає порт, на якому прослуховується сервер
-   [MongoDBDriverMonitoringServerChangedEvent::getPreviousDescription](mongodb-driver-monitoring-serverchangedevent.getpreviousdescription.html) — Повертає попередній опис сервера
-   [MongoDBDriverMonitoringServerChangedEvent::getTopologyId](mongodb-driver-monitoring-serverchangedevent.gettopologyid.html) — Повертає ідентифікатор топології, пов'язаний із цим сервером