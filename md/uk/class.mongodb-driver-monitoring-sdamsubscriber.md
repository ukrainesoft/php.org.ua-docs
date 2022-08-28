Інтерфейс MongoDBDriverMonitoringSDAMSubscriber

-   [« MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandSucceeded](mongodb-driver-monitoring-commandsubscriber.commandsucceeded.html)
    
-   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverChanged »](mongodb-driver-monitoring-sdamsubscriber.serverchanged.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring](mongodb.monitoring.html)
    
-   Інтерфейс MongoDBDriverMonitoringSDAMSubscriber
    

# Інтерфейс MongoDBDriverMonitoringSDAMSubscriber

(mongodb >=1.13.0)

## Вступ

Класи можуть реалізувати цей інтерфейс для реєстрації передплатника подій, який отримує повідомлення про різні події SDAM. Додаткову інформацію дивіться у посібнику з [» Обнаружению и мониторингу серверов](https://github.com/mongodb/specifications/blob/master/source/server-discovery-and-monitoring/server-discovery-and-monitoring.rst) і [» Мониторингу SDAM](https://github.com/mongodb/specifications/blob/master/source/server-discovery-and-monitoring/server-discovery-and-monitoring-monitoring.rst)

## Огляд інтерфейсів

```classsynopsis


    
    
     
      class MongoDB\Driver\Monitoring\SDAMSubscriber
     

     implements 
       MongoDB\Driver\Monitoring\Subscriber {
    

    /* Методы */
    
   abstract public serverChanged(MongoDB\Driver\Monitoring\ServerChangedEvent $event): void
abstract public serverClosed(MongoDB\Driver\Monitoring\ServerClosedEvent $event): void
abstract public serverHeartbeatFailed(MongoDB\Driver\Monitoring\ServerHeartbeatFailedEvent $event): void
abstract public serverHeartbeatStarted(MongoDB\Driver\Monitoring\ServerHeartbeatStartedEvent $event): void
abstract public serverHeartbeatSucceeded(MongoDB\Driver\Monitoring\ServerHeartbeatSucceededEvent $event): void
abstract public serverOpening(MongoDB\Driver\Monitoring\ServerOpeningEvent $event): void
abstract public topologyChanged(MongoDB\Driver\Monitoring\TopologyChangedEvent $event): void
abstract public topologyClosed(MongoDB\Driver\Monitoring\TopologyClosedEvent $event): void
abstract public topologyOpening(MongoDB\Driver\Monitoring\TopologyOpeningEvent $event): void

   }
```

## список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.15.0 | Типи значень, що повертаються для методів оголошені як попередні в PHP 8.0 і новіше, що викликає повідомлення про старіння в коді, який реалізує цей інтерфейс без оголошення відповідних типів значень, що повертаються. Атрибут `#[ReturnTypeWillChange]` може бути доданий, щоб заглушити повідомлення про старіння. |

## Зміст

-   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverChanged](mongodb-driver-monitoring-sdamsubscriber.serverchanged.html) — Метод сповіщення про зміну опису сервера
-   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverClosed](mongodb-driver-monitoring-sdamsubscriber.serverclosed.html) — Метод сповіщення про закриття сервера
-   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverHeartbeatFailed](mongodb-driver-monitoring-sdamsubscriber.serverheartbeatfailed.html) — Метод повідомлення про невдалий heartbeat сервер
-   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverHeartbeatStarted](mongodb-driver-monitoring-sdamsubscriber.serverheartbeatstarted.html) — Метод повідомлення про запущений heartbeat сервер
-   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverHeartbeatSucceeded](mongodb-driver-monitoring-sdamsubscriber.serverheartbeatsucceeded.html) — Метод сповіщення про успішний heartbeat сервер
-   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverOpening](mongodb-driver-monitoring-sdamsubscriber.serveropening.html) — Метод сповіщення про відкриття сервера
-   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber::topologyChanged](mongodb-driver-monitoring-sdamsubscriber.topologychanged.html) — Метод сповіщення про зміну опису топології
-   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber::topologyClosed](mongodb-driver-monitoring-sdamsubscriber.topologyclosed.html) — Метод сповіщення про закриття топології
-   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber::topologyOpening](mongodb-driver-monitoring-sdamsubscriber.topologyopening.html) — Метод повідомлення про відкриття топології