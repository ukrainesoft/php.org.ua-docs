Метод повідомлення про успішну команду

-   [« MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandStarted](mongodb-driver-monitoring-commandsubscriber.commandstarted.html)
    
-   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber »](class.mongodb-driver-monitoring-sdamsubscriber.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandSubscriber](class.mongodb-driver-monitoring-commandsubscriber.html)
    
-   Метод повідомлення про успішну команду
    

# MongoDBDriverMonitoringCommandSubscriber::commandSucceeded

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandSubscriber::commandSucceeded — Метод сповіщення про успішну команду

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\CommandSubscriber::commandSucceeded(MongoDB\Driver\Monitoring\CommandSucceededEvent $event): void
```

Якщо передплатник зареєстровано, драйвер викличе цей метод у разі успішного виконання команди.

### Список параметрів

`event` [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent](class.mongodb-driver-monitoring-commandsucceededevent.html)

Об'єкт події, що містить інформацію про успішну команду.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent](class.mongodb-driver-monitoring-commandsucceededevent.html)
-   [MongoDB\\Driver\\Monitoring\\addSubscriber()](function.mongodb.driver.monitoring.addsubscriber.html) - Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDB\\Driver\\Manager::addSubscriber()](mongodb-driver-manager.addsubscriber.html) - реєструє передплатника на подію моніторингу в даному об'єкті Manager
-   [Мониторинг производительности приложения (Application Performance Monitoring или APM)](mongodb.tutorial.apm.html)