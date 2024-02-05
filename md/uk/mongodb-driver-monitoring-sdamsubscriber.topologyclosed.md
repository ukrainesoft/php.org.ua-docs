---
navigation:
  - mongodb-driver-monitoring-sdamsubscriber.topologychanged.md: '« MongoDB\\Driver\\Monitoring\\SDAMSubscriber::topologyChanged'
  - mongodb-driver-monitoring-sdamsubscriber.topologyopening.md: 'MongoDB\\Driver\\Monitoring\\SDAMSubscriber::topologyOpening »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-sdamsubscriber.md: MongoDB\\Driver\\Monitoring\\SDAMSubscriber
title: 'MongoDB\\Driver\\Monitoring\\SDAMSubscriber::topologyClosed'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\SDAMSubscriber::topologyClosed

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\SDAMSubscriber::topologyClosed — Метод сповіщення про закриття топології

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\SDAMSubscriber::topologyClosed(MongoDB\Driver\Monitoring\TopologyClosedEvent $event): void
```

Якщо передплатник був зареєстрований, драйвер викличе цей метод, якщо топологію буде закрито.

### Список параметрів

`event` [MongoDB\\Driver\\Monitoring\\TopologyClosedEvent](class.mongodb-driver-monitoring-topologyclosedevent.md)) .

Об'єкт події, що містить інформацію про закриту топологію.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\TopologyClosedEvent](class.mongodb-driver-monitoring-topologyclosedevent.md)
-   [MongoDB\\Driver\\Monitoring\\addSubscriber()](function.mongodb.driver.monitoring.addsubscriber.md) \- Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDB\\Driver\\Manager::addSubscriber()](mongodb-driver-manager.addsubscriber.md) \- реєструє передплатника на подію моніторингу в даному об'єкті Manager
