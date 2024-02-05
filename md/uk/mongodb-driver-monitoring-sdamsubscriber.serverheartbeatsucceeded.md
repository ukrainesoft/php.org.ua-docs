---
navigation:
  - mongodb-driver-monitoring-sdamsubscriber.serverheartbeatstarted.md: '« MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverHeartbeatStarted'
  - mongodb-driver-monitoring-sdamsubscriber.serveropening.md: 'MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverOpening »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-sdamsubscriber.md: MongoDB\\Driver\\Monitoring\\SDAMSubscriber
title: 'MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverHeartbeatSucceeded'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverHeartbeatSucceeded

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverHeartbeatSucceeded — Метод сповіщення про успішний сервер heartbeat

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\SDAMSubscriber::serverHeartbeatSucceeded(MongoDB\Driver\Monitoring\ServerHeartbeatSucceededEvent $event): void
```

Якщо передплатник був зареєстрований, драйвер викличе цей метод, у разі успішного виконання heartbeat сервера (тобто команди [» hello](https://www.mongodb.com/docs/manual/reference/command/hello/), викликаної через [» моніторинг сервера](https://github.com/mongodb/specifications/blob/master/source/server-discovery-and-monitoring/server-discovery-and-monitoring.rst)

### Список параметрів

`event` [MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent](class.mongodb-driver-monitoring-serverheartbeatsucceededevent.md)) .

Об'єкт події, що містить інформацію про успішному серцевомусервері.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent](class.mongodb-driver-monitoring-serverheartbeatsucceededevent.md)
-   [MongoDB\\Driver\\Monitoring\\addSubscriber()](function.mongodb.driver.monitoring.addsubscriber.md) \- Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDB\\Driver\\Manager::addSubscriber()](mongodb-driver-manager.addsubscriber.md) \- реєструє передплатника на подію моніторингу в даному об'єкті Manager
