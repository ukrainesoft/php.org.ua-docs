---
navigation:
  - mongodb-driver-monitoring-serverheartbeatstartedevent.isawaited.md: '« MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent::isAwaited'
  - mongodb-driver-monitoring-serverheartbeatsucceededevent.getdurationmicros.md: >-
      MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::getDurationMicros
      »
  - index.md: PHP Manual
  - mongodb.monitoring.md: MongoDB\\Driver\\Monitoring
title: Клас MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent

(mongodb >=1.13.0)

## Вступ

Класс**MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent** інкапсулює інформацію про успішний серцевийсервер.

## Огляд класів

```classsynopsis


    
    
     final
     
      class MongoDB\Driver\Monitoring\ServerHeartbeatSucceededEvent
     
     {
    

    /* Методы */
    
   final public getDurationMicros(): int
final public getHost(): string
final public getPort(): int
final public getReply(): object
final public isAwaited(): bool

   }
```

## Зміст

-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::getDurationMicros](mongodb-driver-monitoring-serverheartbeatsucceededevent.getdurationmicros.md)— Повертає тривалість heartbeat у мікросекундах
-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::getHost](mongodb-driver-monitoring-serverheartbeatsucceededevent.gethost.md)— Повертає ім'я сервера.
-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::getPort](mongodb-driver-monitoring-serverheartbeatsucceededevent.getport.md)— Повертає порт, на якому прослуховується сервер
-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::getReply](mongodb-driver-monitoring-serverheartbeatsucceededevent.getreply.md) \- Повертає документ відповіді heartbeat
-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::isAwaited](mongodb-driver-monitoring-serverheartbeatsucceededevent.isawaited.md)— Повертає, чи використовувався в heartbeat потоковий протокол
