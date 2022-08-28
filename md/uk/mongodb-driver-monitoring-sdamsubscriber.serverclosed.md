Метод сповіщення про закриття сервера

-   [« MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverChanged](mongodb-driver-monitoring-sdamsubscriber.serverchanged.html)
    
-   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverHeartbeatFailed »](mongodb-driver-monitoring-sdamsubscriber.serverheartbeatfailed.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber](class.mongodb-driver-monitoring-sdamsubscriber.html)
    
-   Метод сповіщення про закриття сервера
    

# MongoDBDriverMonitoringSDAMSubscriber::serverClosed

(mongodb >=1.13.0)

MongoDBDriverMonitoringSDAMSubscriber::serverClosed — Метод сповіщення про закриття сервера

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\SDAMSubscriber::serverClosed(MongoDB\Driver\Monitoring\ServerClosedEvent $event): void
```

Якщо передплатник був зареєстрований, драйвер викликає цей метод, якщо сервер закрився.

### Список параметрів

`event` [MongoDB\\Driver\\Monitoring\\ServerClosedEvent](class.mongodb-driver-monitoring-serverclosedevent.html)

Об'єкт події, що містить інформацію про закритий сервер.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\ServerClosedEvent](class.mongodb-driver-monitoring-serverclosedevent.html)
-   [MongoDB\\Driver\\Monitoring\\addSubscriber()](function.mongodb.driver.monitoring.addsubscriber.html) - Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDB\\Driver\\Manager::addSubscriber()](mongodb-driver-manager.addsubscriber.html) - реєструє передплатника на подію моніторингу в даному об'єкті Manager