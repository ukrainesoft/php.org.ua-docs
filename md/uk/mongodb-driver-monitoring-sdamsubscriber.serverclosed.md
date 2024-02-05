---
navigation:
  - mongodb-driver-monitoring-sdamsubscriber.serverchanged.md: '« MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverChanged'
  - mongodb-driver-monitoring-sdamsubscriber.serverheartbeatfailed.md: 'MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverHeartbeatFailed »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-sdamsubscriber.md: MongoDB\\Driver\\Monitoring\\SDAMSubscriber
title: 'MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverClosed'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverClosed

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverClosed — Метод сповіщення про закриття сервера

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\SDAMSubscriber::serverClosed(MongoDB\Driver\Monitoring\ServerClosedEvent $event): void
```

Якщо передплатник був зареєстрований, драйвер викликає цей метод, якщо сервер закрився.

### Список параметрів

`event` [MongoDB\\Driver\\Monitoring\\ServerClosedEvent](class.mongodb-driver-monitoring-serverclosedevent.md)) .

Об'єкт події містить інформацію про закритий сервер.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\ServerClosedEvent](class.mongodb-driver-monitoring-serverclosedevent.md)
-   [MongoDB\\Driver\\Monitoring\\addSubscriber()](function.mongodb.driver.monitoring.addsubscriber.md) \- Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDB\\Driver\\Manager::addSubscriber()](mongodb-driver-manager.addsubscriber.md) \- реєструє передплатника на подію моніторингу в даному об'єкті Manager
