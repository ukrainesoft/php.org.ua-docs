---
navigation:
  - mongodb-driver-monitoring-sdamsubscriber.serverheartbeatsucceeded.md: '« MongoDBDriverMonitoringSDAMSubscriber::serverHeartbeatSucceeded'
  - mongodb-driver-monitoring-sdamsubscriber.topologychanged.md: 'MongoDBDriverMonitoringSDAMSubscriber::topologyChanged »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-sdamsubscriber.md: MongoDBDriverMonitoringSDAMSubscriber
title: 'MongoDBDriverMonitoringSDAMSubscriber::serverOpening'
---
# MongoDBDriverMonitoringSDAMSubscriber::serverOpening

(mongodb >=1.13.0)

MongoDBDriverMonitoringSDAMSubscriber::serverOpening — Метод сповіщення про відкриття сервера

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\SDAMSubscriber::serverOpening(MongoDB\Driver\Monitoring\ServerOpeningEvent $event): void
```

Якщо передплатник був зареєстрований, драйвер викличе цей метод, коли буде відкрито сервер.

### Список параметрів

`event` [MongoDBDriverMonitoringServerOpeningEvent](class.mongodb-driver-monitoring-serveropeningevent.md)

Об'єкт події містить інформацію про відкритий сервер.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverMonitoringServerOpeningEvent](class.mongodb-driver-monitoring-serveropeningevent.md)
-   [MongoDBDriverMonitoringaddSubscriber()](function.mongodb.driver.monitoring.addsubscriber.md) - Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDBDriverManager::addSubscriber()](mongodb-driver-manager.addsubscriber.md) - реєструє передплатника на подію моніторингу в даному об'єкті Manager
