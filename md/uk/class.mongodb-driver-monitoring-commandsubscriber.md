Інтерфейс The MongoDBDriverMonitoringCommandSubscriber

-   [« MongoDB\\Driver\\Monitoring\\TopologyOpeningEvent::getTopologyId](mongodb-driver-monitoring-topologyopeningevent.gettopologyid.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandFailed »](mongodb-driver-monitoring-commandsubscriber.commandfailed.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring](mongodb.monitoring.html)
    
-   Інтерфейс The MongoDBDriverMonitoringCommandSubscriber
    

# Інтерфейс The MongoDBDriverMonitoringCommandSubscriber

(mongodb >=1.3.0)

## Вступ

Класи можуть реалізувати цей інтерфейс для реєстрації передплатника подій, який повідомляється про кожну, успішну або невдалу подію команди. Для детальної інформації дивіться [Мониторинг производительности приложения (Application Performance Monitoring или APM)](mongodb.tutorial.apm.html)

## Огляд інтерфейсів

```classsynopsis



    
     
      class MongoDB\Driver\Monitoring\CommandSubscriber
     

     implements 
       MongoDB\Driver\Monitoring\Subscriber {


    /* Методы */
    
   abstract public commandFailed(MongoDB\Driver\Monitoring\CommandFailedEvent $event): void
abstract public commandStarted(MongoDB\Driver\Monitoring\CommandStartedEvent $event): void
abstract public commandSucceeded(MongoDB\Driver\Monitoring\CommandSucceededEvent $event): void

   }
```

## список змін

| Версия              | Описание                                                                                                                                                                                                                                                                                                                |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PECL mongodb 1.15.0 | Типи значень, що повертаються для методів оголошені як попередні в PHP 8.0 і новіше, що викликає повідомлення про старіння в коді, який реалізує цей інтерфейс без оголошення відповідних типів значень, що повертаються. Атрибут `#[ReturnTypeWillChange]` може бути доданий, щоб заглушити повідомлення про старіння. |

## Зміст

-   [MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandFailed](mongodb-driver-monitoring-commandsubscriber.commandfailed.html) — Метод повідомлення про невдалу команду
-   [MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandStarted](mongodb-driver-monitoring-commandsubscriber.commandstarted.html) — Метод повідомлення про запущену команду
-   [MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandSucceeded](mongodb-driver-monitoring-commandsubscriber.commandsucceeded.html) — Метод повідомлення про успішну команду