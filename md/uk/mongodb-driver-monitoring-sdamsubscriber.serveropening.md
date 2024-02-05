---
navigation:
  - mongodb-driver-monitoring-sdamsubscriber.serverheartbeatsucceeded.md: '« MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverHeartbeatSucceeded'
  - mongodb-driver-monitoring-sdamsubscriber.topologychanged.md: 'MongoDB\\Driver\\Monitoring\\SDAMSubscriber::topologyChanged »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-sdamsubscriber.md: MongoDB\\Driver\\Monitoring\\SDAMSubscriber
title: 'MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverOpening'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverOpening

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverOpening — Метод сповіщення про відкриття сервера

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\SDAMSubscriber::serverOpening(MongoDB\Driver\Monitoring\ServerOpeningEvent $event): void
```

Якщо передплатник був зареєстрований, драйвер викличе цей метод, коли буде відкрито сервер.

### Список параметрів

`event` [MongoDB\\Driver\\Monitoring\\ServerOpeningEvent](class.mongodb-driver-monitoring-serveropeningevent.md)) .

Об'єкт події містить інформацію про відкритий сервер.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\ServerOpeningEvent](class.mongodb-driver-monitoring-serveropeningevent.md)
-   [MongoDB\\Driver\\Monitoring\\addSubscriber()](function.mongodb.driver.monitoring.addsubscriber.md) \- Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDB\\Driver\\Manager::addSubscriber()](mongodb-driver-manager.addsubscriber.md) \- реєструє передплатника на подію моніторингу в даному об'єкті Manager
