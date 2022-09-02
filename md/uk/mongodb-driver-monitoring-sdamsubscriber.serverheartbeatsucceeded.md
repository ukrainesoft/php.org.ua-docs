---
navigation:
  - mongodb-driver-monitoring-sdamsubscriber.serverheartbeatstarted.md: '« MongoDBDriverMonitoringSDAMSubscriber::serverHeartbeatStarted'
  - mongodb-driver-monitoring-sdamsubscriber.serveropening.md: 'MongoDBDriverMonitoringSDAMSubscriber::serverOpening »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-sdamsubscriber.md: MongoDBDriverMonitoringSDAMSubscriber
title: 'MongoDBDriverMonitoringSDAMSubscriber::serverHeartbeatSucceeded'
---
# MongoDBDriverMonitoringSDAMSubscriber::serverHeartbeatSucceeded

(mongodb >=1.13.0)

MongoDBDriverMonitoringSDAMSubscriber::serverHeartbeatSucceeded — Метод сповіщення про успішний сервер heartbeat

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\SDAMSubscriber::serverHeartbeatSucceeded(MongoDB\Driver\Monitoring\ServerHeartbeatSucceededEvent $event): void
```

Якщо передплатник був зареєстрований, драйвер викличе цей метод, у разі успішного виконання heartbeat сервера (тобто команди [» hello](https://www.mongodb.com/docs/manual/reference/command/hello/), викликаної через [» мониторинг сервера](https://github.com/mongodb/specifications/blob/master/source/server-discovery-and-monitoring/server-discovery-and-monitoring.rst)

### Список параметрів

`event` [MongoDBDriverMonitoringServerHeartbeatSucceededEvent](class.mongodb-driver-monitoring-serverheartbeatsucceededevent.md)

Об'єкт події, що містить інформацію про успішному серцевомусервері.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverMonitoringServerHeartbeatSucceededEvent](class.mongodb-driver-monitoring-serverheartbeatsucceededevent.md)
-   [MongoDBDriverMonitoringaddSubscriber()](function.mongodb.driver.monitoring.addsubscriber.md) - Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDBDriverManager::addSubscriber()](mongodb-driver-manager.addsubscriber.md) - реєструє передплатника на подію моніторингу в даному об'єкті Manager
