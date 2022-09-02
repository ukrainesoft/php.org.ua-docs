---
navigation:
  - mongodb-driver-monitoring-sdamsubscriber.serverchanged.md: '« MongoDBDriverMonitoringSDAMSubscriber::serverChanged'
  - mongodb-driver-monitoring-sdamsubscriber.serverheartbeatfailed.md: 'MongoDBDriverMonitoringSDAMSubscriber::serverHeartbeatFailed »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-sdamsubscriber.md: MongoDBDriverMonitoringSDAMSubscriber
title: 'MongoDBDriverMonitoringSDAMSubscriber::serverClosed'
---
# MongoDBDriverMonitoringSDAMSubscriber::serverClosed

(mongodb >=1.13.0)

MongoDBDriverMonitoringSDAMSubscriber::serverClosed — Метод сповіщення про закриття сервера

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\SDAMSubscriber::serverClosed(MongoDB\Driver\Monitoring\ServerClosedEvent $event): void
```

Якщо передплатник був зареєстрований, драйвер викликає цей метод, якщо сервер закрився.

### Список параметрів

`event` [MongoDBDriverMonitoringServerClosedEvent](class.mongodb-driver-monitoring-serverclosedevent.md)

Об'єкт події, що містить інформацію про закритий сервер.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverMonitoringServerClosedEvent](class.mongodb-driver-monitoring-serverclosedevent.md)
-   [MongoDBDriverMonitoringaddSubscriber()](function.mongodb.driver.monitoring.addsubscriber.md) - Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDBDriverManager::addSubscriber()](mongodb-driver-manager.addsubscriber.md) - реєструє передплатника на подію моніторингу в даному об'єкті Manager
