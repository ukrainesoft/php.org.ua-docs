---
navigation:
  - mongodb-driver-monitoring-commandsubscriber.commandfailed.md: '« MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandFailed'
  - mongodb-driver-monitoring-commandsubscriber.commandsucceeded.md: 'MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandSucceeded »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandsubscriber.md: MongoDB\\Driver\\Monitoring\\CommandSubscriber
title: 'MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandStarted'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandStarted

(mongodb >=1.3.0)

MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandStarted — Метод сповіщення про запущену команду

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\CommandSubscriber::commandStarted(MongoDB\Driver\Monitoring\CommandStartedEvent $event): void
```

Якщо передплатник зареєстровано, драйвер викличе цей метод під час запуску команди.

### Список параметрів

`event` [MongoDB\\Driver\\Monitoring\\CommandStartedEvent](class.mongodb-driver-monitoring-commandstartedevent.md)) .

Об'єкт події, що містить інформацію про запущену команду.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent](class.mongodb-driver-monitoring-commandstartedevent.md)
-   [MongoDB\\Driver\\Monitoring\\addSubscriber()](function.mongodb.driver.monitoring.addsubscriber.md) \- Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDB\\Driver\\Manager::addSubscriber()](mongodb-driver-manager.addsubscriber.md) \- реєструє передплатника на подію моніторингу в даному об'єкті Manager
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
