Клас MongoDBDriverMonitoringServerHeartbeatSucceededEvent

-   [« MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent::isAwaited](mongodb-driver-monitoring-serverheartbeatstartedevent.isawaited.html)
    
-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::getDurationMicros »](mongodb-driver-monitoring-serverheartbeatsucceededevent.getdurationmicros.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring](mongodb.monitoring.html)
    
-   Клас MongoDBDriverMonitoringServerHeartbeatSucceededEvent
    

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

-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::getDurationMicros](mongodb-driver-monitoring-serverheartbeatsucceededevent.getdurationmicros.html) — Повертає тривалість heartbeat у мікросекундах
-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::getHost](mongodb-driver-monitoring-serverheartbeatsucceededevent.gethost.html) — Повертає ім'я сервера.
-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::getPort](mongodb-driver-monitoring-serverheartbeatsucceededevent.getport.html) — Повертає порт, на якому прослуховується сервер
-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::getReply](mongodb-driver-monitoring-serverheartbeatsucceededevent.getreply.html) - Повертає документ відповіді heartbeat
-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::isAwaited](mongodb-driver-monitoring-serverheartbeatsucceededevent.isawaited.html) — Повертає, чи використовувався в heartbeat потоковий протокол