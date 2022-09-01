---
navigation:
  - function.mongodb.driver.monitoring.removesubscriber.md: « MongoDBDriverMonitoringremoveSubscriber
  - mongodb-driver-monitoring-commandfailedevent.getcommandname.html: 'MongoDBDriverMonitoringCommandFailedEvent::getCommandName »'
  - index.md: PHP Manual
  - mongodb.monitoring.md: MongoDBDriverMonitoring
title: Клас MongoDBDriverMonitoringCommandFailedEvent
---
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

-   [MongoDBDriverMonitoringCommandFailedEvent::getCommandName](mongodb-driver-monitoring-commandfailedevent.getcommandname.md) - Повертає ім'я команди
-   [MongoDBDriverMonitoringCommandFailedEvent::getDurationMicros](mongodb-driver-monitoring-commandfailedevent.getdurationmicros.md) — Повертає тривалість команди у мікросекундах
-   [MongoDBDriverMonitoringCommandFailedEvent::getError](mongodb-driver-monitoring-commandfailedevent.geterror.md) — Повертає виняток, пов'язаний із невдалою командою
-   [MongoDBDriverMonitoringCommandFailedEvent::getOperationId](mongodb-driver-monitoring-commandfailedevent.getoperationid.md) - Повертає ідентифікатор операції команди
-   [MongoDBDriverMonitoringCommandFailedEvent::getReply](mongodb-driver-monitoring-commandfailedevent.getreply.md) - Повертає документ відповіді команди
-   [MongoDBDriverMonitoringCommandFailedEvent::getRequestId](mongodb-driver-monitoring-commandfailedevent.getrequestid.md) - Повертає ідентифікатор запиту команди
-   [MongoDBDriverMonitoringCommandFailedEvent::getServer](mongodb-driver-monitoring-commandfailedevent.getserver.md) — Повертає сервер, на якому було виконано команду
-   [MongoDBDriverMonitoringCommandFailedEvent::getServerConnectionId](mongodb-driver-monitoring-commandfailedevent.getserverconnectionid.md) — Повертає ідентифікатор з'єднання із сервером для команди
-   [MongoDBDriverMonitoringCommandFailedEvent::getServiceId](mongodb-driver-monitoring-commandfailedevent.getserviceid.md) — Повертає ідентифікатор служби балансувальника навантаження для команди
