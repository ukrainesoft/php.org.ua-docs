---
navigation:
  - mongodb-driver-monitoring-topologyopeningevent.gettopologyid.html: '« MongoDBDriverMonitoringTopologyOpeningEvent::getTopologyId'
  - mongodb-driver-monitoring-commandsubscriber.commandfailed.html: 'MongoDBDriverMonitoringCommandSubscriber::commandFailed »'
  - index.md: PHP Manual
  - mongodb.monitoring.md: MongoDBDriverMonitoring
title: Інтерфейс The MongoDBDriverMonitoringCommandSubscriber
---
# Інтерфейс The MongoDBDriverMonitoringCommandSubscriber

(mongodb >=1.3.0)

## Вступ

Класи можуть реалізувати цей інтерфейс для реєстрації передплатника подій, який повідомляється про кожну, успішну або невдалу подію команди. Для детальної інформації дивіться [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)

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

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.15.0 | Типи значень, що повертаються для методів оголошені як попередні в PHP 8.0 і новіше, що викликає повідомлення про старіння в коді, який реалізує цей інтерфейс без оголошення відповідних типів значень, що повертаються. Атрибут `#[ReturnTypeWillChange]` може бути доданий, щоб заглушити повідомлення про старіння. |

## Зміст

-   [MongoDBDriverMonitoringCommandSubscriber::commandFailed](mongodb-driver-monitoring-commandsubscriber.commandfailed.html) — Метод повідомлення про невдалу команду
-   [MongoDBDriverMonitoringCommandSubscriber::commandStarted](mongodb-driver-monitoring-commandsubscriber.commandstarted.html) — Метод повідомлення про запущену команду
-   [MongoDBDriverMonitoringCommandSubscriber::commandSucceeded](mongodb-driver-monitoring-commandsubscriber.commandsucceeded.html) — Метод повідомлення про успішну команду
