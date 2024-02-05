---
navigation:
  - mongodb-driver-monitoring-commandstartedevent.getserviceid.md: '« MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getServiceId'
  - mongodb-driver-monitoring-commandsucceededevent.getcommandname.md: 'MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getCommandName »'
  - index.md: PHP Manual
  - mongodb.monitoring.md: MongoDB\\Driver\\Monitoring
title: Клас MongoDB\\Driver\\Monitoring\\CommandSucceededEvent
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\Driver\\Monitoring\\CommandSucceededEvent

(mongodb >=1.3.0)

## Вступ

Класс**MongoDB\\Driver\\Monitoring\\CommandSucceededEvent** містить інформацію про успішну команду.

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

-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getCommandName](mongodb-driver-monitoring-commandsucceededevent.getcommandname.md) \- Повертає ім'я команди
-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getDurationMicros](mongodb-driver-monitoring-commandsucceededevent.getdurationmicros.md)— Повертає тривалість команди у мікросекундах
-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getOperationId](mongodb-driver-monitoring-commandsucceededevent.getoperationid.md) \- Повертає ідентифікатор операції команди
-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getReply](mongodb-driver-monitoring-commandsucceededevent.getreply.md) \- Повертає документ відповіді команди
-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getRequestId](mongodb-driver-monitoring-commandsucceededevent.getrequestid.md) \- Повертає ідентифікатор запиту команди
-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getServer](mongodb-driver-monitoring-commandsucceededevent.getserver.md)— Повертає сервер, на якому було виконано команду
-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getServerConnectionId](mongodb-driver-monitoring-commandsucceededevent.getserverconnectionid.md)— Повертає ідентифікатор з'єднання із сервером для команди
-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getServiceId](mongodb-driver-monitoring-commandsucceededevent.getserviceid.md)— Повертає ідентифікатор служби балансувальника навантаження для команди
