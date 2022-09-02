---
navigation:
  - mongodb-driver-monitoring-serverheartbeatstartedevent.isawaited.md: '« MongoDBDriverMonitoringServerHeartbeatStartedEvent::isAwaited'
  - mongodb-driver-monitoring-serverheartbeatsucceededevent.getdurationmicros.md: 'MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getDurationMicros »'
  - index.md: PHP Manual
  - mongodb.monitoring.md: MongoDBDriverMonitoring
title: Клас MongoDBDriverMonitoringServerHeartbeatSucceededEvent
---
# Клас MongoDBDriverMonitoringServerHeartbeatSucceededEvent

(mongodb >=1.13.0)

## Вступ

Клас **MongoDBDriverMonitoringServerHeartbeatSucceededEvent** Інкапсулює інформацію про успішний серцевийсервер.

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

-   [MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getDurationMicros](mongodb-driver-monitoring-serverheartbeatsucceededevent.getdurationmicros.md) — Повертає тривалість heartbeat у мікросекундах
-   [MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getHost](mongodb-driver-monitoring-serverheartbeatsucceededevent.gethost.md) — Повертає ім'я сервера.
-   [MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getPort](mongodb-driver-monitoring-serverheartbeatsucceededevent.getport.md) — Повертає порт, на якому прослуховується сервер
-   [MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getReply](mongodb-driver-monitoring-serverheartbeatsucceededevent.getreply.md) - Повертає документ відповіді heartbeat
-   [MongoDBDriverMonitoringServerHeartbeatSucceededEvent::isAwaited](mongodb-driver-monitoring-serverheartbeatsucceededevent.isawaited.md) — Повертає, чи використовувався в heartbeat потоковий протокол
