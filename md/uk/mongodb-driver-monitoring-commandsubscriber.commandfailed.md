---
navigation:
  - class.mongodb-driver-monitoring-commandsubscriber.md: « MongoDB\\Driver\\Monitoring\\CommandSubscriber
  - mongodb-driver-monitoring-commandsubscriber.commandstarted.md: 'MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandStarted »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandsubscriber.md: MongoDB\\Driver\\Monitoring\\CommandSubscriber
title: 'MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandFailed'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandFailed

(mongodb >=1.3.0)

MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandFailed — Метод сповіщення про невдалу команду

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\CommandSubscriber::commandFailed(MongoDB\Driver\Monitoring\CommandFailedEvent $event): void
```

Якщо передплатник зареєстровано, драйвер викличе цей метод у разі помилки команди.

### Список параметрів

`event` [MongoDB\\Driver\\Monitoring\\CommandFailedEvent](class.mongodb-driver-monitoring-commandfailedevent.md)) .

Об'єкт події, що містить інформацію про невдалу команду.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent](class.mongodb-driver-monitoring-commandfailedevent.md)
-   [MongoDB\\Driver\\Monitoring\\addSubscriber()](function.mongodb.driver.monitoring.addsubscriber.md) \- Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDB\\Driver\\Manager::addSubscriber()](mongodb-driver-manager.addsubscriber.md) \- реєструє передплатника на подію моніторингу в даному об'єкті Manager
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
