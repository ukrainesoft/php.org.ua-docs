---
navigation:
  - mongodb-driver-monitoring-commandfailedevent.getserviceid.md: '« MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getServiceId'
  - mongodb-driver-monitoring-commandstartedevent.getcommand.md: 'MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getCommand »'
  - index.md: PHP Manual
  - mongodb.monitoring.md: MongoDB\\Driver\\Monitoring
title: Клас MongoDB\\Driver\\Monitoring\\CommandStartedEvent
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\Driver\\Monitoring\\CommandStartedEvent

(mongodb >=1.3.0)

## Вступ

Класс**MongoDB\\Driver\\Monitoring\\CommandStartedEvent** містить інформацію про запущену команду.

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

-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getCommand](mongodb-driver-monitoring-commandstartedevent.getcommand.md) \- Повертає документ команди
-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getCommandName](mongodb-driver-monitoring-commandstartedevent.getcommandname.md) \- Повертає ім'я команди
-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getDatabaseName](mongodb-driver-monitoring-commandstartedevent.getdatabasename.md)— Повертає базу даних, на якій виконувалась команда
-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getOperationId](mongodb-driver-monitoring-commandstartedevent.getoperationid.md) \- Повертає ідентифікатор операції команди
-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getRequestId](mongodb-driver-monitoring-commandstartedevent.getrequestid.md) \- Повертає ідентифікатор запиту команди
-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getServer](mongodb-driver-monitoring-commandstartedevent.getserver.md)— Повертає сервер, на якому було виконано команду
-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getServerConnectionId](mongodb-driver-monitoring-commandstartedevent.getserverconnectionid.md)— Повертає ідентифікатор з'єднання із сервером для команди
-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getServiceId](mongodb-driver-monitoring-commandstartedevent.getserviceid.md)— Повертає ідентифікатор служби балансувальника навантаження для команди
