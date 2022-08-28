Метод сповіщення про зміну опису сервера

-   [« MongoDB\\Driver\\Monitoring\\SDAMSubscriber](class.mongodb-driver-monitoring-sdamsubscriber.html)
    
-   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverClosed »](mongodb-driver-monitoring-sdamsubscriber.serverclosed.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber](class.mongodb-driver-monitoring-sdamsubscriber.html)
    
-   Метод сповіщення про зміну опису сервера
    

# MongoDBDriverMonitoringSDAMSubscriber::serverChanged

(mongodb >=1.13.0)

MongoDBDriverMonitoringSDAMSubscriber::serverChanged — Метод сповіщення про зміну опису сервера

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\SDAMSubscriber::serverChanged(MongoDB\Driver\Monitoring\ServerChangedEvent $event): void
```

Якщо передплатник був зареєстрований, драйвер викликатиме цей метод, якщо опис сервера змінився.

### Список параметрів

`event` [MongoDB\\Driver\\Monitoring\\ServerChangedEvent](class.mongodb-driver-monitoring-serverchangedevent.html)

Об'єкт події, що містить інформацію про змінений опис сервера.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\ServerChangedEvent](class.mongodb-driver-monitoring-serverchangedevent.html)
-   [MongoDB\\Driver\\Monitoring\\addSubscriber()](function.mongodb.driver.monitoring.addsubscriber.html) - Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDB\\Driver\\Manager::addSubscriber()](mongodb-driver-manager.addsubscriber.html) - реєструє передплатника на подію моніторингу в даному об'єкті Manager