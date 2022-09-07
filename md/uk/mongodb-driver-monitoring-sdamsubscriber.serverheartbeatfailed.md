---
navigation:
  - mongodb-driver-monitoring-sdamsubscriber.serverclosed.md: '« MongoDBDriverMonitoringSDAMSubscriber::serverClosed'
  - mongodb-driver-monitoring-sdamsubscriber.serverheartbeatstarted.md: 'MongoDBDriverMonitoringSDAMSubscriber::serverHeartbeatStarted »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-sdamsubscriber.md: MongoDBDriverMonitoringSDAMSubscriber
title: 'MongoDBDriverMonitoringSDAMSubscriber::serverHeartbeatFailed'
---
# MongoDBDriverMonitoringSDAMSubscriber::serverHeartbeatFailed

(mongodb >=1.13.0)

MongoDBDriverMonitoringSDAMSubscriber::serverHeartbeatFailed — Метод сповіщення про невдалий сервер heartbeat

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\SDAMSubscriber::serverHeartbeatFailed(MongoDB\Driver\Monitoring\ServerHeartbeatFailedEvent $event): void
```

Якщо передплатник був зареєстрований, драйвер викличе цей метод, у разі виникнення помилки на heartbeat сервера (тобто команди [» hello](https://www.mongodb.com/docs/manual/reference/command/hello/), викликаної через [» мониторинг сервера](https://github.com/mongodb/specifications/blob/master/source/server-discovery-and-monitoring/server-discovery-and-monitoring.rst)

### Список параметрів

`event` [MongoDBDriverMonitoringServerHeartbeatFailedEvent](class.mongodb-driver-monitoring-serverheartbeatfailedevent.md)

Об'єкт події, що містить інформацію про непрацюючому серцевомусервері.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverMonitoringServerHeartbeatFailedEvent](class.mongodb-driver-monitoring-serverheartbeatfailedevent.md)
-   [MongoDBDriverMonitoringaddSubscriber()](function.mongodb.driver.monitoring.addsubscriber.md) - Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDBDriverManager::addSubscriber()](mongodb-driver-manager.addsubscriber.md) - реєструє передплатника на подію моніторингу в даному об'єкті Manager
