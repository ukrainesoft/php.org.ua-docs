---
navigation:
  - mongodb-driver-monitoring-commandsubscriber.commandstarted.md: '« MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandStarted'
  - class.mongodb-driver-monitoring-logsubscriber.md: MongoDB\\Driver\\Monitoring\\LogSubscriber »
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandsubscriber.md: MongoDB\\Driver\\Monitoring\\CommandSubscriber
title: 'MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandSucceeded'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandSucceeded

(mongodb >=1.3.0)

MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandSucceeded — Метод сповіщення про успішну команду

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\CommandSubscriber::commandSucceeded(MongoDB\Driver\Monitoring\CommandSucceededEvent $event): void
```

Якщо передплатник зареєстровано, драйвер викличе цей метод у разі успішного виконання команди.

### Список параметрів

`event` [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent](class.mongodb-driver-monitoring-commandsucceededevent.md)) .

Об'єкт події, що містить інформацію про успішну команду.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent](class.mongodb-driver-monitoring-commandsucceededevent.md)
-   [MongoDB\\Driver\\Monitoring\\addSubscriber()](function.mongodb.driver.monitoring.addsubscriber.md) \- Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDB\\Driver\\Manager::addSubscriber()](mongodb-driver-manager.addsubscriber.md) \- реєструє передплатника на подію моніторингу в даному об'єкті Manager
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
