---
navigation:
  - mongodb-driver-monitoring-sdamsubscriber.serveropening.md: '« MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverOpening'
  - mongodb-driver-monitoring-sdamsubscriber.topologyclosed.md: 'MongoDB\\Driver\\Monitoring\\SDAMSubscriber::topologyClosed »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-sdamsubscriber.md: MongoDB\\Driver\\Monitoring\\SDAMSubscriber
title: 'MongoDB\\Driver\\Monitoring\\SDAMSubscriber::topologyChanged'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\SDAMSubscriber::topologyChanged

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\SDAMSubscriber::topologyChanged — Метод сповіщення про зміну опису топології

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\SDAMSubscriber::topologyChanged(MongoDB\Driver\Monitoring\TopologyChangedEvent $event): void
```

Якщо передплатник був зареєстрований, драйвер викличе цей метод, якщо опис топології зміниться.

### Список параметрів

`event` [MongoDB\\Driver\\Monitoring\\TopologyChangedEvent](class.mongodb-driver-monitoring-topologychangedevent.md)) .

Об'єкт події, що містить інформацію про змінений опис топології.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\TopologyChangedEvent](class.mongodb-driver-monitoring-topologychangedevent.md)
-   [MongoDB\\Driver\\Monitoring\\addSubscriber()](function.mongodb.driver.monitoring.addsubscriber.md) \- Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDB\\Driver\\Manager::addSubscriber()](mongodb-driver-manager.addsubscriber.md) \- реєструє передплатника на подію моніторингу в даному об'єкті Manager
