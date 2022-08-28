Метод сповіщення про зміну опису топології

-   [« MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverOpening](mongodb-driver-monitoring-sdamsubscriber.serveropening.html)
    
-   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber::topologyClosed »](mongodb-driver-monitoring-sdamsubscriber.topologyclosed.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber](class.mongodb-driver-monitoring-sdamsubscriber.html)
    
-   Метод сповіщення про зміну опису топології
    

# MongoDBDriverMonitoringSDAMSubscriber::topologyChanged

(mongodb >=1.13.0)

MongoDBDriverMonitoringSDAMSubscriber::topologyChanged — Метод сповіщення про зміну опису топології

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\SDAMSubscriber::topologyChanged(MongoDB\Driver\Monitoring\TopologyChangedEvent $event): void
```

Якщо передплатник був зареєстрований, драйвер викличе цей метод, якщо опис топології зміниться.

### Список параметрів

`event` [MongoDB\\Driver\\Monitoring\\TopologyChangedEvent](class.mongodb-driver-monitoring-topologychangedevent.html)

Об'єкт події, що містить інформацію про змінений опис топології.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\TopologyChangedEvent](class.mongodb-driver-monitoring-topologychangedevent.html)
-   [MongoDB\\Driver\\Monitoring\\addSubscriber()](function.mongodb.driver.monitoring.addsubscriber.html) - Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDB\\Driver\\Manager::addSubscriber()](mongodb-driver-manager.addsubscriber.html) - реєструє передплатника на подію моніторингу в даному об'єкті Manager