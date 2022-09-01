---
navigation:
  - mongodb-driver-monitoring-serveropeningevent.gettopologyid.html: '« MongoDBDriverMonitoringServerOpeningEvent::getTopologyId'
  - mongodb-driver-monitoring-serverheartbeatfailedevent.getdurationmicros.html: 'MongoDBDriverMonitoringServerHeartbeatFailedEvent::getDurationMicros »'
  - index.md: PHP Manual
  - mongodb.monitoring.md: MongoDBDriverMonitoring
title: Клас MongoDBDriverMonitoringServerHeartbeatFailedEvent
---
# Клас MongoDBDriverMonitoringServerHeartbeatFailedEvent

(mongodb >=1.13.0)

## Вступ

Клас **MongoDBDriverMonitoringServerHeartbeatFailedEvent** Інкапсулює інформацію про невдалий серцевийсервер.

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

-   [MongoDBDriverMonitoringServerHeartbeatFailedEvent::getDurationMicros](mongodb-driver-monitoring-serverheartbeatfailedevent.getdurationmicros.html) — Повертає тривалість heartbeat у мікросекундах
-   [MongoDBDriverMonitoringServerHeartbeatFailedEvent::getError](mongodb-driver-monitoring-serverheartbeatfailedevent.geterror.html) — Повертає виняток, пов'язаний із невдалим виконанням heartbeat
-   [MongoDBDriverMonitoringServerHeartbeatFailedEvent::getHost](mongodb-driver-monitoring-serverheartbeatfailedevent.gethost.html) — Повертає ім'я сервера.
-   [MongoDBDriverMonitoringServerHeartbeatFailedEvent::getPort](mongodb-driver-monitoring-serverheartbeatfailedevent.getport.html) — Повертає порт, на якому прослуховується сервер
-   [MongoDBDriverMonitoringServerHeartbeatFailedEvent::isAwaited](mongodb-driver-monitoring-serverheartbeatfailedevent.isawaited.html) — Повертає, чи використовувався в heartbeat потоковий протокол
