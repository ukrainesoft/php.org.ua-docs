---
navigation:
  - mongodb-driver-monitoring-serveropeningevent.gettopologyid.md: '« MongoDB\\Driver\\Monitoring\\ServerOpeningEvent::getTopologyId'
  - mongodb-driver-monitoring-serverheartbeatfailedevent.getdurationmicros.md: >-
      MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::getDurationMicros
      »
  - index.md: PHP Manual
  - mongodb.monitoring.md: MongoDB\\Driver\\Monitoring
title: Клас MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent

(mongodb >=1.13.0)

## Вступ

Класс**MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent** Інкапсулює інформацію про невдалий серцевийсервер.

## Огляд класів

```classsynopsis


    
    
     final
     
      class MongoDB\Driver\Monitoring\ServerHeartbeatFailedEvent
     
     {
    

    /* Методы */
    
   final public getDurationMicros(): int
final public getError(): Exception
final public getHost(): string
final public getPort(): int
final public isAwaited(): bool

   }
```

## Зміст

-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::getDurationMicros](mongodb-driver-monitoring-serverheartbeatfailedevent.getdurationmicros.md)— Повертає тривалість heartbeat у мікросекундах
-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::getError](mongodb-driver-monitoring-serverheartbeatfailedevent.geterror.md)— Повертає виняток, пов'язаний із невдалим виконанням heartbeat
-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::getHost](mongodb-driver-monitoring-serverheartbeatfailedevent.gethost.md)— Повертає ім'я сервера.
-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::getPort](mongodb-driver-monitoring-serverheartbeatfailedevent.getport.md)— Повертає порт, на якому прослуховується сервер
-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::isAwaited](mongodb-driver-monitoring-serverheartbeatfailedevent.isawaited.md)— Повертає, чи використовувався в heartbeat потоковий протокол
