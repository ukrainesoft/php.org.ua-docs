---
navigation:
  - mongodb-driver-monitoring-sdamsubscriber.topologyclosed.md: '« MongoDB\\Driver\\Monitoring\\SDAMSubscriber::topologyClosed'
  - class.mongodb-driver-monitoring-subscriber.md: MongoDB\\Driver\\Monitoring\\Subscriber »
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-sdamsubscriber.md: MongoDB\\Driver\\Monitoring\\SDAMSubscriber
title: 'MongoDB\\Driver\\Monitoring\\SDAMSubscriber::topologyOpening'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\SDAMSubscriber::topologyOpening

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\SDAMSubscriber::topologyOpening — Метод сповіщення про відкриття топології

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\SDAMSubscriber::topologyOpening(MongoDB\Driver\Monitoring\TopologyOpeningEvent $event): void
```

Якщо передплатник був зареєстрований, драйвер викличе цей метод, коли топологія буде відкрита.

### Список параметрів

`event` [MongoDB\\Driver\\Monitoring\\TopologyOpeningEvent](class.mongodb-driver-monitoring-topologyopeningevent.md)) .

Об'єкт події, що містить інформацію про відкриту топологію.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\TopologyOpeningEvent](class.mongodb-driver-monitoring-topologyopeningevent.md)
-   [MongoDB\\Driver\\Monitoring\\addSubscriber()](function.mongodb.driver.monitoring.addsubscriber.md) \- Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDB\\Driver\\Manager::addSubscriber()](mongodb-driver-manager.addsubscriber.md) \- реєструє передплатника на подію моніторингу в даному об'єкті Manager
