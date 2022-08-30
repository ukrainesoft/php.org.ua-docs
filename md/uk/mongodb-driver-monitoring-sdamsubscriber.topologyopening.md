Метод сповіщення про відкриття топології

-   [« MongoDBDriverMonitoringSDAMSubscriber::topologyClosed](mongodb-driver-monitoring-sdamsubscriber.topologyclosed.html)
    
-   [MongoDBDriverMonitoringSubscriber »](class.mongodb-driver-monitoring-subscriber.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverMonitoringSDAMSubscriber](class.mongodb-driver-monitoring-sdamsubscriber.html)
    
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

`event` [MongoDBDriverMonitoringTopologyOpeningEvent](class.mongodb-driver-monitoring-topologyopeningevent.html)

Об'єкт події, що містить інформацію про відкриту топологію.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverMonitoringTopologyOpeningEvent](class.mongodb-driver-monitoring-topologyopeningevent.html)
-   [MongoDBDriverMonitoringaddSubscriber()](function.mongodb.driver.monitoring.addsubscriber.md) - Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDBDriverManager::addSubscriber()](mongodb-driver-manager.addsubscriber.html) - реєструє передплатника на подію моніторингу в даному об'єкті Manager