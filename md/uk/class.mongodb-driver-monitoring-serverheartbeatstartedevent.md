---
navigation:
  - mongodb-driver-monitoring-serverheartbeatfailedevent.isawaited.md: '« MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::isAwaited'
  - mongodb-driver-monitoring-serverheartbeatstartedevent.gethost.md: 'MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent::getHost »'
  - index.md: PHP Manual
  - mongodb.monitoring.md: MongoDB\\Driver\\Monitoring
title: Клас MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent

(mongodb >=1.13.0)

## Вступ

Класс**MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent** інкапсулює інформацію про запущений heartbeat сервер.

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

-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent::getHost](mongodb-driver-monitoring-serverheartbeatstartedevent.gethost.md)— Повертає ім'я сервера.
-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent::getPort](mongodb-driver-monitoring-serverheartbeatstartedevent.getport.md)— Повертає порт, на якому прослуховується сервер
-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent::isAwaited](mongodb-driver-monitoring-serverheartbeatstartedevent.isawaited.md)— Повертає, чи використовувався в heartbeat потоковий протокол
