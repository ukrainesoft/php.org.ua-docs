Метод сповіщення про закриття топології

-   [« MongoDB\\Driver\\Monitoring\\SDAMSubscriber::topologyChanged](mongodb-driver-monitoring-sdamsubscriber.topologychanged.html)
    
-   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber::topologyOpening »](mongodb-driver-monitoring-sdamsubscriber.topologyopening.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber](class.mongodb-driver-monitoring-sdamsubscriber.html)
    
-   Метод сповіщення про закриття топології
    

# MongoDBDriverMonitoringSDAMSubscriber::topologyClosed

(mongodb >=1.13.0)

MongoDBDriverMonitoringSDAMSubscriber::topologyClosed — Метод сповіщення про закриття топології

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\SDAMSubscriber::topologyClosed(MongoDB\Driver\Monitoring\TopologyClosedEvent $event): void
```

Якщо передплатник був зареєстрований, драйвер викличе цей метод, якщо топологію буде закрито.

### Список параметрів

`event` [MongoDB\\Driver\\Monitoring\\TopologyClosedEvent](class.mongodb-driver-monitoring-topologyclosedevent.html)

Об'єкт події, що містить інформацію про закриту топологію.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\TopologyClosedEvent](class.mongodb-driver-monitoring-topologyclosedevent.html)
-   [MongoDB\\Driver\\Monitoring\\addSubscriber()](function.mongodb.driver.monitoring.addsubscriber.html) - Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDB\\Driver\\Manager::addSubscriber()](mongodb-driver-manager.addsubscriber.html) - реєструє передплатника на подію моніторингу в даному об'єкті Manager