---
navigation:
  - mongodb-driver-monitoring-sdamsubscriber.serverclosed.md: '« MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverClosed'
  - mongodb-driver-monitoring-sdamsubscriber.serverheartbeatstarted.md: 'MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverHeartbeatStarted »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-sdamsubscriber.md: MongoDB\\Driver\\Monitoring\\SDAMSubscriber
title: 'MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverHeartbeatFailed'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverHeartbeatFailed

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverHeartbeatFailed — Метод сповіщення про невдалий сервер heartbeat

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\SDAMSubscriber::serverHeartbeatFailed(MongoDB\Driver\Monitoring\ServerHeartbeatFailedEvent $event): void
```

Якщо передплатник був зареєстрований, драйвер викличе цей метод, у разі виникнення помилки на heartbeat сервера (тобто команди [» hello](https://www.mongodb.com/docs/manual/reference/command/hello/), викликаної через [» моніторинг сервера](https://github.com/mongodb/specifications/blob/master/source/server-discovery-and-monitoring/server-discovery-and-monitoring.rst)

### Список параметрів

`event` [MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent](class.mongodb-driver-monitoring-serverheartbeatfailedevent.md)) .

Об'єкт події, що містить інформацію про непрацюючому серцевомусервері.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent](class.mongodb-driver-monitoring-serverheartbeatfailedevent.md)
-   [MongoDB\\Driver\\Monitoring\\addSubscriber()](function.mongodb.driver.monitoring.addsubscriber.md) \- Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDB\\Driver\\Manager::addSubscriber()](mongodb-driver-manager.addsubscriber.md) \- реєструє передплатника на подію моніторингу в даному об'єкті Manager
