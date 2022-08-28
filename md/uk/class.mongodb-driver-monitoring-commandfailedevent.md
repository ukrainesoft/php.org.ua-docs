Клас MongoDBDriverMonitoringCommandFailedEvent

-   [« MongoDB\\Driver\\Monitoring\\removeSubscriber](function.mongodb.driver.monitoring.removesubscriber.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getCommandName »](mongodb-driver-monitoring-commandfailedevent.getcommandname.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring](mongodb.monitoring.html)
    
-   Клас MongoDBDriverMonitoringCommandFailedEvent
    

# Клас MongoDBDriverMonitoringCommandFailedEvent

(mongodb >=1.3.0)

## Вступ

Клас **MongoDBDriverMonitoringCommandFailedEvent** містить інформацію про невдалу команду.

## Огляд класів

```classsynopsis



    
     final
     
      class MongoDB\Driver\Monitoring\CommandFailedEvent
     
     {


    /* Методы */
    
   final public getCommandName(): string
final public getDurationMicros(): int
final public getError(): Exception
final public getOperationId(): string
final public getReply(): object
final public getRequestId(): string
final public getServer(): MongoDB\Driver\Server
final public getServerConnectionId(): ?int
final public getServiceId(): ?MongoDB\BSON\ObjectId

   }
```

## Зміст

-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getCommandName](mongodb-driver-monitoring-commandfailedevent.getcommandname.html) - Повертає ім'я команди
-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getDurationMicros](mongodb-driver-monitoring-commandfailedevent.getdurationmicros.html) — Повертає тривалість команди у мікросекундах
-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getError](mongodb-driver-monitoring-commandfailedevent.geterror.html) — Повертає виняток, пов'язаний із невдалою командою
-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getOperationId](mongodb-driver-monitoring-commandfailedevent.getoperationid.html) - Повертає ідентифікатор операції команди
-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getReply](mongodb-driver-monitoring-commandfailedevent.getreply.html) - Повертає документ відповіді команди
-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getRequestId](mongodb-driver-monitoring-commandfailedevent.getrequestid.html) - Повертає ідентифікатор запиту команди
-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getServer](mongodb-driver-monitoring-commandfailedevent.getserver.html) — Повертає сервер, на якому було виконано команду
-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getServerConnectionId](mongodb-driver-monitoring-commandfailedevent.getserverconnectionid.html) — Повертає ідентифікатор з'єднання із сервером для команди
-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getServiceId](mongodb-driver-monitoring-commandfailedevent.getserviceid.html) — Повертає ідентифікатор служби балансувальника навантаження для команди