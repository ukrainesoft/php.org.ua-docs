---
navigation:
  - mongodb-driver-monitoring-commandsucceededevent.getserviceid.md: '« MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getServiceId'
  - mongodb-driver-monitoring-serverchangedevent.gethost.md: 'MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getHost »'
  - index.md: PHP Manual
  - mongodb.monitoring.md: MongoDB\\Driver\\Monitoring
title: Клас MongoDB\\Driver\\Monitoring\\ServerChangedEvent
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\Driver\\Monitoring\\ServerChangedEvent

(mongodb >=1.13.0)

## Вступ

Класс**MongoDB\\Driver\\Monitoring\\ServerChangedEvent**инкапсулирует информацию об изменении описания сервера.

## Огляд класів

```classsynopsis


    
    
     final
     
      class MongoDB\Driver\Monitoring\ServerChangedEvent
     
     {
    

    /* Методы */
    
   final public getHost(): string
final public getNewDescription(): MongoDB\Driver\ServerDescription
final public getPort(): int
final public getPreviousDescription(): MongoDB\Driver\ServerDescription
final public getTopologyId(): MongoDB\BSON\ObjectId

   }
```

## Зміст

-   [MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getHost](mongodb-driver-monitoring-serverchangedevent.gethost.md)— Повертає ім'я сервера.
-   [MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getNewDescription](mongodb-driver-monitoring-serverchangedevent.getnewdescription.md)— Повертає новий опис сервера
-   [MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getPort](mongodb-driver-monitoring-serverchangedevent.getport.md)— Повертає порт, на якому прослуховується сервер
-   [MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getPreviousDescription](mongodb-driver-monitoring-serverchangedevent.getpreviousdescription.md)— Повертає попередній опис сервера
-   [MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getTopologyId](mongodb-driver-monitoring-serverchangedevent.gettopologyid.md)— Повертає ідентифікатор топології, пов'язаний із цим сервером
