Метод повідомлення про успішний heartbeat сервер

-   [« MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverHeartbeatStarted](mongodb-driver-monitoring-sdamsubscriber.serverheartbeatstarted.html)
    
-   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverOpening »](mongodb-driver-monitoring-sdamsubscriber.serveropening.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber](class.mongodb-driver-monitoring-sdamsubscriber.html)
    
-   Метод повідомлення про успішний heartbeat сервер
    

# MongoDBDriverMonitoringSDAMSubscriber::serverHeartbeatSucceeded

(mongodb >=1.13.0)

MongoDBDriverMonitoringSDAMSubscriber::serverHeartbeatSucceeded — Метод сповіщення про успішний сервер heartbeat

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\SDAMSubscriber::serverHeartbeatSucceeded(MongoDB\Driver\Monitoring\ServerHeartbeatSucceededEvent $event): void
```

Якщо передплатник був зареєстрований, драйвер викличе цей метод, у разі успішного виконання heartbeat сервера (тобто команди [» hello](https://www.mongodb.com/docs/manual/reference/command/hello/), викликаної через [» мониторинг сервера](https://github.com/mongodb/specifications/blob/master/source/server-discovery-and-monitoring/server-discovery-and-monitoring.rst)

### Список параметрів

`event` [MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent](class.mongodb-driver-monitoring-serverheartbeatsucceededevent.html)

Об'єкт події, що містить інформацію про успішному серцевомусервері.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent](class.mongodb-driver-monitoring-serverheartbeatsucceededevent.html)
-   [MongoDB\\Driver\\Monitoring\\addSubscriber()](function.mongodb.driver.monitoring.addsubscriber.html) - Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDB\\Driver\\Manager::addSubscriber()](mongodb-driver-manager.addsubscriber.html) - реєструє передплатника на подію моніторингу в даному об'єкті Manager