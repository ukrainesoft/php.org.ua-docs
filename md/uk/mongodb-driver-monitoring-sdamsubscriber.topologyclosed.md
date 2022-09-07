---
navigation:
  - mongodb-driver-monitoring-sdamsubscriber.topologychanged.md: '« MongoDBDriverMonitoringSDAMSubscriber::topologyChanged'
  - mongodb-driver-monitoring-sdamsubscriber.topologyopening.md: 'MongoDBDriverMonitoringSDAMSubscriber::topologyOpening »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-sdamsubscriber.md: MongoDBDriverMonitoringSDAMSubscriber
title: 'MongoDBDriverMonitoringSDAMSubscriber::topologyClosed'
---
# MongoDBDriverMonitoringSDAMSubscriber::topologyClosed

(mongodb >=1.13.0)

MongoDBDriverMonitoringSDAMSubscriber::topologyClosed — Метод сповіщення про закриття топології

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\SDAMSubscriber::topologyClosed(MongoDB\Driver\Monitoring\TopologyClosedEvent $event): void
```

Якщо передплатник був зареєстрований, драйвер викличе цей метод, якщо топологію буде закрито.

### Список параметрів

`event` [MongoDBDriverMonitoringTopologyClosedEvent](class.mongodb-driver-monitoring-topologyclosedevent.md)

Об'єкт події, що містить інформацію про закриту топологію.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverMonitoringTopologyClosedEvent](class.mongodb-driver-monitoring-topologyclosedevent.md)
-   [MongoDBDriverMonitoringaddSubscriber()](function.mongodb.driver.monitoring.addsubscriber.md) - Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDBDriverManager::addSubscriber()](mongodb-driver-manager.addsubscriber.md) - реєструє передплатника на подію моніторингу в даному об'єкті Manager
