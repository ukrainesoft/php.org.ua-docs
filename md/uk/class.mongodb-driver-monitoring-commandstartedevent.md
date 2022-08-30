Клас MongoDBDriverMonitoringCommandStartedEvent

-   [« MongoDBDriverMonitoringCommandFailedEvent::getServiceId](mongodb-driver-monitoring-commandfailedevent.getserviceid.html)
    
-   [MongoDBDriverMonitoringCommandStartedEvent::getCommand »](mongodb-driver-monitoring-commandstartedevent.getcommand.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverMonitoring](mongodb.monitoring.html)
    
-   Клас MongoDBDriverMonitoringCommandStartedEvent
    

# Клас MongoDBDriverMonitoringCommandStartedEvent

(mongodb >=1.3.0)

## Вступ

Клас **MongoDBDriverMonitoringCommandStartedEvent** містить інформацію про запущену команду.

## Огляд класів

```classsynopsis



    
     final
     
      class MongoDB\Driver\Monitoring\CommandStartedEvent
     
     {


    /* Методы */
    
   final public getCommand(): object
final public getCommandName(): string
final public getDatabaseName(): string
final public getOperationId(): string
final public getRequestId(): string
final public getServer(): MongoDB\Driver\Server
final public getServerConnectionId(): ?int
final public getServiceId(): ?MongoDB\BSON\ObjectId

   }
```

## Зміст

-   [MongoDBDriverMonitoringCommandStartedEvent::getCommand](mongodb-driver-monitoring-commandstartedevent.getcommand.html) - Повертає документ команди
-   [MongoDBDriverMonitoringCommandStartedEvent::getCommandName](mongodb-driver-monitoring-commandstartedevent.getcommandname.html) - Повертає ім'я команди
-   [MongoDBDriverMonitoringCommandStartedEvent::getDatabaseName](mongodb-driver-monitoring-commandstartedevent.getdatabasename.html) — Повертає базу даних, на якій виконувалась команда
-   [MongoDBDriverMonitoringCommandStartedEvent::getOperationId](mongodb-driver-monitoring-commandstartedevent.getoperationid.html) - Повертає ідентифікатор операції команди
-   [MongoDBDriverMonitoringCommandStartedEvent::getRequestId](mongodb-driver-monitoring-commandstartedevent.getrequestid.html) - Повертає ідентифікатор запиту команди
-   [MongoDBDriverMonitoringCommandStartedEvent::getServer](mongodb-driver-monitoring-commandstartedevent.getserver.html) — Повертає сервер, на якому було виконано команду
-   [MongoDBDriverMonitoringCommandStartedEvent::getServerConnectionId](mongodb-driver-monitoring-commandstartedevent.getserverconnectionid.html) — Повертає ідентифікатор з'єднання із сервером для команди
-   [MongoDBDriverMonitoringCommandStartedEvent::getServiceId](mongodb-driver-monitoring-commandstartedevent.getserviceid.html) — Повертає ідентифікатор служби балансувальника навантаження для команди