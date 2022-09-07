---
navigation:
  - mongodb-driver-monitoring-serverheartbeatfailedevent.isawaited.md: '« MongoDBDriverMonitoringServerHeartbeatFailedEvent::isAwaited'
  - mongodb-driver-monitoring-serverheartbeatstartedevent.gethost.md: 'MongoDBDriverMonitoringServerHeartbeatStartedEvent::getHost »'
  - index.md: PHP Manual
  - mongodb.monitoring.md: MongoDBDriverMonitoring
title: Клас MongoDBDriverMonitoringServerHeartbeatStartedEvent
---
# Клас MongoDBDriverMonitoringServerHeartbeatStartedEvent

(mongodb >=1.13.0)

## Вступ

Клас **MongoDBDriverMonitoringServerHeartbeatStartedEvent** інкапсулює інформацію про запущений heartbeat сервер.

## Огляд класів

```classsynopsis


    
    
     final
     
      class MongoDB\Driver\Monitoring\ServerHeartbeatStartedEvent
     
     {
    

    /* Методы */
    
   final public getHost(): string
final public getPort(): int
final public isAwaited(): bool

   }
```

## Зміст

-   [MongoDBDriverMonitoringServerHeartbeatStartedEvent::getHost](mongodb-driver-monitoring-serverheartbeatstartedevent.gethost.md) — Повертає ім'я сервера.
-   [MongoDBDriverMonitoringServerHeartbeatStartedEvent::getPort](mongodb-driver-monitoring-serverheartbeatstartedevent.getport.md) — Повертає порт, на якому прослуховується сервер
-   [MongoDBDriverMonitoringServerHeartbeatStartedEvent::isAwaited](mongodb-driver-monitoring-serverheartbeatstartedevent.isawaited.md) — Повертає, чи використовувався в heartbeat потоковий протокол
