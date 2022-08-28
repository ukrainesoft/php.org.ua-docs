Клас MongoDBDriverMonitoringServerHeartbeatStartedEvent

-   [« MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::isAwaited](mongodb-driver-monitoring-serverheartbeatfailedevent.isawaited.html)
    
-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent::getHost »](mongodb-driver-monitoring-serverheartbeatstartedevent.gethost.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring](mongodb.monitoring.html)
    
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

-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent::getHost](mongodb-driver-monitoring-serverheartbeatstartedevent.gethost.html) — Повертає ім'я сервера.
-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent::getPort](mongodb-driver-monitoring-serverheartbeatstartedevent.getport.html) — Повертає порт, на якому прослуховується сервер
-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent::isAwaited](mongodb-driver-monitoring-serverheartbeatstartedevent.isawaited.html) — Повертає, чи використовувався в heartbeat потоковий протокол