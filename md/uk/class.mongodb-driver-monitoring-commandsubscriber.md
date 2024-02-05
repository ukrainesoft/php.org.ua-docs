---
navigation:
  - mongodb-driver-monitoring-topologyopeningevent.gettopologyid.md: '« MongoDB\\Driver\\Monitoring\\TopologyOpeningEvent::getTopologyId'
  - mongodb-driver-monitoring-commandsubscriber.commandfailed.md: 'MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandFailed »'
  - index.md: PHP Manual
  - mongodb.monitoring.md: MongoDB\\Driver\\Monitoring
title: Інтерфейс The MongoDB\\Driver\\Monitoring\\CommandSubscriber
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс The MongoDB\\Driver\\Monitoring\\CommandSubscriber

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

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.15.0 | Типи значень, що повертаються для методів оголошені як попередні в PHP 8.0 і новіше, що викликає повідомлення про старіння в коді, який реалізує цей інтерфейс без оголошення відповідних типів значень, що повертаються. Атрибут `#[ReturnTypeWillChange]` може бути доданий, щоб заглушити повідомлення про старіння. |

## Зміст

-   [MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandFailed](mongodb-driver-monitoring-commandsubscriber.commandfailed.md)— Метод повідомлення про невдалу команду
-   [MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandStarted](mongodb-driver-monitoring-commandsubscriber.commandstarted.md)— Метод повідомлення про запущену команду
-   [MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandSucceeded](mongodb-driver-monitoring-commandsubscriber.commandsucceeded.md)— Метод повідомлення про успішну команду
