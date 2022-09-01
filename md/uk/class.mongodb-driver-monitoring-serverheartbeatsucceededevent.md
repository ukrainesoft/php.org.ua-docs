---
navigation:
  - mongodb-driver-monitoring-serverheartbeatstartedevent.isawaited.html: '« MongoDBDriverMonitoringServerHeartbeatStartedEvent::isAwaited'
  - mongodb-driver-monitoring-serverheartbeatsucceededevent.getdurationmicros.html: 'MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getDurationMicros »'
  - index.html: PHP Manual
  - mongodb.monitoring.html: MongoDBDriverMonitoring
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

-   [MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getDurationMicros](mongodb-driver-monitoring-serverheartbeatsucceededevent.getdurationmicros.html) — Повертає тривалість heartbeat у мікросекундах
-   [MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getHost](mongodb-driver-monitoring-serverheartbeatsucceededevent.gethost.html) — Повертає ім'я сервера.
-   [MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getPort](mongodb-driver-monitoring-serverheartbeatsucceededevent.getport.html) — Повертає порт, на якому прослуховується сервер
-   [MongoDBDriverMonitoringServerHeartbeatSucceededEvent::getReply](mongodb-driver-monitoring-serverheartbeatsucceededevent.getreply.html) - Повертає документ відповіді heartbeat
-   [MongoDBDriverMonitoringServerHeartbeatSucceededEvent::isAwaited](mongodb-driver-monitoring-serverheartbeatsucceededevent.isawaited.html) — Повертає, чи використовувався в heartbeat потоковий протокол
