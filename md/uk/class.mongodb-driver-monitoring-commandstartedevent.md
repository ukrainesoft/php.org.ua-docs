---
navigation:
  - mongodb-driver-monitoring-commandfailedevent.getserviceid.md: '« MongoDBDriverMonitoringCommandFailedEvent::getServiceId'
  - mongodb-driver-monitoring-commandstartedevent.getcommand.md: 'MongoDBDriverMonitoringCommandStartedEvent::getCommand »'
  - index.md: PHP Manual
  - mongodb.monitoring.md: MongoDBDriverMonitoring
title: Клас MongoDBDriverMonitoringCommandStartedEvent
---
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

-   [MongoDBDriverMonitoringCommandStartedEvent::getCommand](mongodb-driver-monitoring-commandstartedevent.getcommand.md) - Повертає документ команди
-   [MongoDBDriverMonitoringCommandStartedEvent::getCommandName](mongodb-driver-monitoring-commandstartedevent.getcommandname.md) - Повертає ім'я команди
-   [MongoDBDriverMonitoringCommandStartedEvent::getDatabaseName](mongodb-driver-monitoring-commandstartedevent.getdatabasename.md) — Повертає базу даних, на якій виконувалась команда
-   [MongoDBDriverMonitoringCommandStartedEvent::getOperationId](mongodb-driver-monitoring-commandstartedevent.getoperationid.md) - Повертає ідентифікатор операції команди
-   [MongoDBDriverMonitoringCommandStartedEvent::getRequestId](mongodb-driver-monitoring-commandstartedevent.getrequestid.md) - Повертає ідентифікатор запиту команди
-   [MongoDBDriverMonitoringCommandStartedEvent::getServer](mongodb-driver-monitoring-commandstartedevent.getserver.md) — Повертає сервер, на якому було виконано команду
-   [MongoDBDriverMonitoringCommandStartedEvent::getServerConnectionId](mongodb-driver-monitoring-commandstartedevent.getserverconnectionid.md) — Повертає ідентифікатор з'єднання із сервером для команди
-   [MongoDBDriverMonitoringCommandStartedEvent::getServiceId](mongodb-driver-monitoring-commandstartedevent.getserviceid.md) — Повертає ідентифікатор служби балансувальника навантаження для команди
