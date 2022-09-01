---
navigation:
  - mongodb-driver-monitoring-sdamsubscriber.serveropening.html: '« MongoDBDriverMonitoringSDAMSubscriber::serverOpening'
  - mongodb-driver-monitoring-sdamsubscriber.topologyclosed.html: 'MongoDBDriverMonitoringSDAMSubscriber::topologyClosed »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-sdamsubscriber.html: MongoDBDriverMonitoringSDAMSubscriber
title: 'MongoDBDriverMonitoringSDAMSubscriber::topologyChanged'
---
# MongoDBDriverMonitoringSDAMSubscriber::topologyChanged

(mongodb >=1.13.0)

MongoDBDriverMonitoringSDAMSubscriber::topologyChanged — Метод сповіщення про зміну опису топології

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\SDAMSubscriber::topologyChanged(MongoDB\Driver\Monitoring\TopologyChangedEvent $event): void
```

Якщо передплатник був зареєстрований, драйвер викличе цей метод, якщо опис топології зміниться.

### Список параметрів

`event` [MongoDBDriverMonitoringTopologyChangedEvent](class.mongodb-driver-monitoring-topologychangedevent.md)

Об'єкт події, що містить інформацію про змінений опис топології.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverMonitoringTopologyChangedEvent](class.mongodb-driver-monitoring-topologychangedevent.md)
-   [MongoDBDriverMonitoringaddSubscriber()](function.mongodb.driver.monitoring.addsubscriber.md) - Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDBDriverManager::addSubscriber()](mongodb-driver-manager.addsubscriber.md) - реєструє передплатника на подію моніторингу в даному об'єкті Manager
