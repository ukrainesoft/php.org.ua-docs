Клас MongoDBDriverMonitoringCommandSucceedEvent

-   [« MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getServiceId](mongodb-driver-monitoring-commandstartedevent.getserviceid.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getCommandName »](mongodb-driver-monitoring-commandsucceededevent.getcommandname.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring](mongodb.monitoring.html)
    
-   Клас MongoDBDriverMonitoringCommandSucceedEvent
    

# Клас MongoDBDriverMonitoringCommandSucceedEvent

(mongodb >=1.3.0)

## Вступ

Клас **MongoDBDriverMonitoringCommandSucceedEvent** містить інформацію про успішну команду.

## Огляд класів

```classsynopsis



    
     final
     
      class MongoDB\Driver\Monitoring\CommandSucceededEvent
     
     {


    /* Методы */
    
   final public getCommandName(): string
final public getDurationMicros(): int
final public getOperationId(): string
final public getReply(): object
final public getRequestId(): string
final public getServer(): MongoDB\Driver\Server
final public getServerConnectionId(): ?int
final public getServiceId(): ?MongoDB\BSON\ObjectId

   }
```

## Зміст

-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getCommandName](mongodb-driver-monitoring-commandsucceededevent.getcommandname.html) - Повертає ім'я команди
-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getDurationMicros](mongodb-driver-monitoring-commandsucceededevent.getdurationmicros.html) — Повертає тривалість команди у мікросекундах
-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getOperationId](mongodb-driver-monitoring-commandsucceededevent.getoperationid.html) - Повертає ідентифікатор операції команди
-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getReply](mongodb-driver-monitoring-commandsucceededevent.getreply.html) - Повертає документ відповіді команди
-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getRequestId](mongodb-driver-monitoring-commandsucceededevent.getrequestid.html) - Повертає ідентифікатор запиту команди
-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getServer](mongodb-driver-monitoring-commandsucceededevent.getserver.html) — Повертає сервер, на якому було виконано команду
-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getServerConnectionId](mongodb-driver-monitoring-commandsucceededevent.getserverconnectionid.html) — Повертає ідентифікатор з'єднання із сервером для команди
-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getServiceId](mongodb-driver-monitoring-commandsucceededevent.getserviceid.html) — Повертає ідентифікатор служби балансувальника навантаження для команди