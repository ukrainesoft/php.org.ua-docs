Метод повідомлення про запущений heartbeat сервер

-   [« MongoDBDriverMonitoringSDAMSubscriber::serverHeartbeatFailed](mongodb-driver-monitoring-sdamsubscriber.serverheartbeatfailed.html)
    
-   [MongoDBDriverMonitoringSDAMSubscriber::serverHeartbeatSucceeded »](mongodb-driver-monitoring-sdamsubscriber.serverheartbeatsucceeded.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverMonitoringSDAMSubscriber](class.mongodb-driver-monitoring-sdamsubscriber.html)
    
-   Метод повідомлення про запущений heartbeat сервер
    

# MongoDBDriverMonitoringSDAMSubscriber::serverHeartbeatStarted

(mongodb >=1.13.0)

MongoDBDriverMonitoringSDAMSubscriber::serverHeartbeatStarted — Метод сповіщення про запущений сервер heartbeat

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\SDAMSubscriber::serverHeartbeatStarted(MongoDB\Driver\Monitoring\ServerHeartbeatStartedEvent $event): void
```

Якщо передплатник був зареєстрований, драйвер викличе цей метод під час запуску heartbeat сервера (тобто команди [» hello](https://www.mongodb.com/docs/manual/reference/command/hello/), викликаної через [» мониторинг сервера](https://github.com/mongodb/specifications/blob/master/source/server-discovery-and-monitoring/server-discovery-and-monitoring.rst)

### Список параметрів

`event` [MongoDBDriverMonitoringServerHeartbeatStartedEvent](class.mongodb-driver-monitoring-serverheartbeatstartedevent.html)

Об'єктом події, що містить інформацію про запущеному серцевомусервері.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverMonitoringServerHeartbeatStartedEvent](class.mongodb-driver-monitoring-serverheartbeatstartedevent.html)
-   [MongoDBDriverMonitoringaddSubscriber()](function.mongodb.driver.monitoring.addsubscriber.md) - Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDBDriverManager::addSubscriber()](mongodb-driver-manager.addsubscriber.html) - реєструє передплатника на подію моніторингу в даному об'єкті Manager