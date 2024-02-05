---
navigation:
  - function.mongodb.driver.monitoring.removesubscriber.md: « MongoDB\\Driver\\Monitoring\\removeSubscriber
  - mongodb-driver-monitoring-commandfailedevent.getcommandname.md: 'MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getCommandName »'
  - index.md: PHP Manual
  - mongodb.monitoring.md: MongoDB\\Driver\\Monitoring
title: Клас MongoDB\\Driver\\Monitoring\\CommandFailedEvent
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\Driver\\Monitoring\\CommandFailedEvent

(mongodb >=1.3.0)

## Вступ

Класс**MongoDB\\Driver\\Monitoring\\CommandFailedEvent** містить інформацію про невдалу команду.

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

-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getCommandName](mongodb-driver-monitoring-commandfailedevent.getcommandname.md) \- Повертає ім'я команди
-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getDurationMicros](mongodb-driver-monitoring-commandfailedevent.getdurationmicros.md)— Повертає тривалість команди у мікросекундах
-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getError](mongodb-driver-monitoring-commandfailedevent.geterror.md)— Повертає виняток, пов'язаний із невдалою командою
-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getOperationId](mongodb-driver-monitoring-commandfailedevent.getoperationid.md) \- Повертає ідентифікатор операції команди
-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getReply](mongodb-driver-monitoring-commandfailedevent.getreply.md) \- Повертає документ відповіді команди
-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getRequestId](mongodb-driver-monitoring-commandfailedevent.getrequestid.md) \- Повертає ідентифікатор запиту команди
-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getServer](mongodb-driver-monitoring-commandfailedevent.getserver.md)— Повертає сервер, на якому було виконано команду
-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getServerConnectionId](mongodb-driver-monitoring-commandfailedevent.getserverconnectionid.md)— Повертає ідентифікатор з'єднання із сервером для команди
-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getServiceId](mongodb-driver-monitoring-commandfailedevent.getserviceid.md)— Повертає ідентифікатор служби балансувальника навантаження для команди
