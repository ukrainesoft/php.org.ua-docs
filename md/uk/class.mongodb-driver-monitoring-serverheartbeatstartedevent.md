Клас MongoDBDriverMonitoringServerHeartbeatStartedEvent

-   [« MongoDBDriverMonitoringServerHeartbeatFailedEvent::isAwaited](mongodb-driver-monitoring-serverheartbeatfailedevent.isawaited.html)
    
-   [MongoDBDriverMonitoringServerHeartbeatStartedEvent::getHost »](mongodb-driver-monitoring-serverheartbeatstartedevent.gethost.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverMonitoring](mongodb.monitoring.html)
    
-   Клас MongoDBDriverMonitoringServerHeartbeatStartedEvent
    

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

-   [MongoDBDriverMonitoringServerHeartbeatStartedEvent::getHost](mongodb-driver-monitoring-serverheartbeatstartedevent.gethost.html) — Повертає ім'я сервера.
-   [MongoDBDriverMonitoringServerHeartbeatStartedEvent::getPort](mongodb-driver-monitoring-serverheartbeatstartedevent.getport.html) — Повертає порт, на якому прослуховується сервер
-   [MongoDBDriverMonitoringServerHeartbeatStartedEvent::isAwaited](mongodb-driver-monitoring-serverheartbeatstartedevent.isawaited.html) — Повертає, чи використовувався в heartbeat потоковий протокол