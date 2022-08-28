Клас MongoDBDriverMonitoringCommandStartedEvent

-   [« MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getServiceId](mongodb-driver-monitoring-commandfailedevent.getserviceid.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getCommand »](mongodb-driver-monitoring-commandstartedevent.getcommand.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring](mongodb.monitoring.html)
    
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

-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getCommand](mongodb-driver-monitoring-commandstartedevent.getcommand.html) - Повертає документ команди
-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getCommandName](mongodb-driver-monitoring-commandstartedevent.getcommandname.html) - Повертає ім'я команди
-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getDatabaseName](mongodb-driver-monitoring-commandstartedevent.getdatabasename.html) — Повертає базу даних, на якій виконувалась команда
-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getOperationId](mongodb-driver-monitoring-commandstartedevent.getoperationid.html) - Повертає ідентифікатор операції команди
-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getRequestId](mongodb-driver-monitoring-commandstartedevent.getrequestid.html) - Повертає ідентифікатор запиту команди
-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getServer](mongodb-driver-monitoring-commandstartedevent.getserver.html) — Повертає сервер, на якому було виконано команду
-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getServerConnectionId](mongodb-driver-monitoring-commandstartedevent.getserverconnectionid.html) — Повертає ідентифікатор з'єднання із сервером для команди
-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getServiceId](mongodb-driver-monitoring-commandstartedevent.getserviceid.html) — Повертає ідентифікатор служби балансувальника навантаження для команди