---
navigation:
  - mongodb-driver-monitoring-serveropeningevent.gettopologyid.md: '« MongoDBDriverMonitoringServerOpeningEvent::getTopologyId'
  - mongodb-driver-monitoring-serverheartbeatfailedevent.getdurationmicros.md: 'MongoDBDriverMonitoringServerHeartbeatFailedEvent::getDurationMicros »'
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

-   [MongoDBDriverMonitoringServerHeartbeatFailedEvent::getDurationMicros](mongodb-driver-monitoring-serverheartbeatfailedevent.getdurationmicros.md) — Повертає тривалість heartbeat у мікросекундах
-   [MongoDBDriverMonitoringServerHeartbeatFailedEvent::getError](mongodb-driver-monitoring-serverheartbeatfailedevent.geterror.md) — Повертає виняток, пов'язаний із невдалим виконанням heartbeat
-   [MongoDBDriverMonitoringServerHeartbeatFailedEvent::getHost](mongodb-driver-monitoring-serverheartbeatfailedevent.gethost.md) — Повертає ім'я сервера.
-   [MongoDBDriverMonitoringServerHeartbeatFailedEvent::getPort](mongodb-driver-monitoring-serverheartbeatfailedevent.getport.md) — Повертає порт, на якому прослуховується сервер
-   [MongoDBDriverMonitoringServerHeartbeatFailedEvent::isAwaited](mongodb-driver-monitoring-serverheartbeatfailedevent.isawaited.md) — Повертає, чи використовувався в heartbeat потоковий протокол
