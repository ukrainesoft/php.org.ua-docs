Метод сповіщення про відкриття топології

-   [« MongoDB\\Driver\\Monitoring\\SDAMSubscriber::topologyClosed](mongodb-driver-monitoring-sdamsubscriber.topologyclosed.html)
    
-   [MongoDB\\Driver\\Monitoring\\Subscriber »](class.mongodb-driver-monitoring-subscriber.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber](class.mongodb-driver-monitoring-sdamsubscriber.html)
    
-   Метод сповіщення про відкриття топології
    

# MongoDBDriverMonitoringSDAMSubscriber::topologyOpening

(mongodb >=1.13.0)

MongoDBDriverMonitoringSDAMSubscriber::topologyOpening — Метод сповіщення про відкриття топології

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\SDAMSubscriber::topologyOpening(MongoDB\Driver\Monitoring\TopologyOpeningEvent $event): void
```

Якщо передплатник був зареєстрований, драйвер викличе цей метод, коли топологія буде відкрита.

### Список параметрів

`event` [MongoDB\\Driver\\Monitoring\\TopologyOpeningEvent](class.mongodb-driver-monitoring-topologyopeningevent.html)

Об'єкт події, що містить інформацію про відкриту топологію.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\TopologyOpeningEvent](class.mongodb-driver-monitoring-topologyopeningevent.html)
-   [MongoDB\\Driver\\Monitoring\\addSubscriber()](function.mongodb.driver.monitoring.addsubscriber.html) - Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDB\\Driver\\Manager::addSubscriber()](mongodb-driver-manager.addsubscriber.html) - реєструє передплатника на подію моніторингу в даному об'єкті Manager