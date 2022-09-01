---
navigation:
  - mongodb-driver-monitoring-commandstartedevent.getserviceid.html: '« MongoDBDriverMonitoringCommandStartedEvent::getServiceId'
  - mongodb-driver-monitoring-commandsucceededevent.getcommandname.html: 'MongoDBDriverMonitoringCommandSucceededEvent::getCommandName »'
  - index.md: PHP Manual
  - mongodb.monitoring.md: MongoDBDriverMonitoring
title: Клас MongoDBDriverMonitoringCommandSucceedEvent
---
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

-   [MongoDBDriverMonitoringCommandSucceededEvent::getCommandName](mongodb-driver-monitoring-commandsucceededevent.getcommandname.html) - Повертає ім'я команди
-   [MongoDBDriverMonitoringCommandSucceededEvent::getDurationMicros](mongodb-driver-monitoring-commandsucceededevent.getdurationmicros.html) — Повертає тривалість команди у мікросекундах
-   [MongoDBDriverMonitoringCommandSucceededEvent::getOperationId](mongodb-driver-monitoring-commandsucceededevent.getoperationid.html) - Повертає ідентифікатор операції команди
-   [MongoDBDriverMonitoringCommandSucceededEvent::getReply](mongodb-driver-monitoring-commandsucceededevent.getreply.html) - Повертає документ відповіді команди
-   [MongoDBDriverMonitoringCommandSucceededEvent::getRequestId](mongodb-driver-monitoring-commandsucceededevent.getrequestid.html) - Повертає ідентифікатор запиту команди
-   [MongoDBDriverMonitoringCommandSucceededEvent::getServer](mongodb-driver-monitoring-commandsucceededevent.getserver.html) — Повертає сервер, на якому було виконано команду
-   [MongoDBDriverMonitoringCommandSucceededEvent::getServerConnectionId](mongodb-driver-monitoring-commandsucceededevent.getserverconnectionid.html) — Повертає ідентифікатор з'єднання із сервером для команди
-   [MongoDBDriverMonitoringCommandSucceededEvent::getServiceId](mongodb-driver-monitoring-commandsucceededevent.getserviceid.html) — Повертає ідентифікатор служби балансувальника навантаження для команди
