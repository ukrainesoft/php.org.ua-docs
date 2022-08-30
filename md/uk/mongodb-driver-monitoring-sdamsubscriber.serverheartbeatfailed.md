Метод повідомлення про невдалий heartbeat сервер

-   [« MongoDBDriverMonitoringSDAMSubscriber::serverClosed](mongodb-driver-monitoring-sdamsubscriber.serverclosed.html)
    
-   [MongoDBDriverMonitoringSDAMSubscriber::serverHeartbeatStarted »](mongodb-driver-monitoring-sdamsubscriber.serverheartbeatstarted.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverMonitoringSDAMSubscriber](class.mongodb-driver-monitoring-sdamsubscriber.html)
    
-   Метод повідомлення про невдалий heartbeat сервер
    

# MongoDBDriverMonitoringSDAMSubscriber::serverHeartbeatFailed

(mongodb >=1.13.0)

MongoDBDriverMonitoringSDAMSubscriber::serverHeartbeatFailed — Метод сповіщення про невдалий сервер heartbeat

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\SDAMSubscriber::serverHeartbeatFailed(MongoDB\Driver\Monitoring\ServerHeartbeatFailedEvent $event): void
```

Якщо передплатник був зареєстрований, драйвер викличе цей метод, у разі виникнення помилки на heartbeat сервера (тобто команди [» hello](https://www.mongodb.com/docs/manual/reference/command/hello/), викликаної через [» мониторинг сервера](https://github.com/mongodb/specifications/blob/master/source/server-discovery-and-monitoring/server-discovery-and-monitoring.rst)

### Список параметрів

`event` [MongoDBDriverMonitoringServerHeartbeatFailedEvent](class.mongodb-driver-monitoring-serverheartbeatfailedevent.html)

Об'єкт події, що містить інформацію про непрацюючому серцевомусервері.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverMonitoringServerHeartbeatFailedEvent](class.mongodb-driver-monitoring-serverheartbeatfailedevent.html)
-   [MongoDBDriverMonitoringaddSubscriber()](function.mongodb.driver.monitoring.addsubscriber.html) - Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDBDriverManager::addSubscriber()](mongodb-driver-manager.addsubscriber.html) - реєструє передплатника на подію моніторингу в даному об'єкті Manager