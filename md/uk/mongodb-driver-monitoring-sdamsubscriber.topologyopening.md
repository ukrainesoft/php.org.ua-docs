---
navigation:
  - mongodb-driver-monitoring-sdamsubscriber.topologyclosed.html: '« MongoDBDriverMonitoringSDAMSubscriber::topologyClosed'
  - class.mongodb-driver-monitoring-subscriber.html: MongoDBDriverMonitoringSubscriber »
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-sdamsubscriber.html: MongoDBDriverMonitoringSDAMSubscriber
title: 'MongoDBDriverMonitoringSDAMSubscriber::topologyOpening'
---
# MongoDBDriverMonitoringSDAMSubscriber::topologyOpening

(mongodb >=1.13.0)

MongoDBDriverMonitoringSDAMSubscriber::topologyOpening — Метод сповіщення про відкриття топології

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\SDAMSubscriber::topologyOpening(MongoDB\Driver\Monitoring\TopologyOpeningEvent $event): void
```

Якщо передплатник був зареєстрований, драйвер викличе цей метод, коли топологія буде відкрита.

### Список параметрів

`event` [MongoDBDriverMonitoringTopologyOpeningEvent](class.mongodb-driver-monitoring-topologyopeningevent.md)

Об'єкт події, що містить інформацію про відкриту топологію.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverMonitoringTopologyOpeningEvent](class.mongodb-driver-monitoring-topologyopeningevent.md)
-   [MongoDBDriverMonitoringaddSubscriber()](function.mongodb.driver.monitoring.addsubscriber.md) - Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDBDriverManager::addSubscriber()](mongodb-driver-manager.addsubscriber.md) - реєструє передплатника на подію моніторингу в даному об'єкті Manager
