Метод повідомлення про запущену команду

-   [« MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandFailed](mongodb-driver-monitoring-commandsubscriber.commandfailed.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandSucceeded »](mongodb-driver-monitoring-commandsubscriber.commandsucceeded.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandSubscriber](class.mongodb-driver-monitoring-commandsubscriber.html)
    
-   Метод повідомлення про запущену команду
    

# MongoDBDriverMonitoringCommandSubscriber::commandStarted

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandSubscriber::commandStarted — Метод сповіщення про запущену команду

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\CommandSubscriber::commandStarted(MongoDB\Driver\Monitoring\CommandStartedEvent $event): void
```

Якщо передплатник зареєстровано, драйвер викличе цей метод під час запуску команди.

### Список параметрів

`event` [MongoDB\\Driver\\Monitoring\\CommandStartedEvent](class.mongodb-driver-monitoring-commandstartedevent.html)

Об'єкт події, що містить інформацію про запущену команду.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent](class.mongodb-driver-monitoring-commandstartedevent.html)
-   [MongoDB\\Driver\\Monitoring\\addSubscriber()](function.mongodb.driver.monitoring.addsubscriber.html) - Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDB\\Driver\\Manager::addSubscriber()](mongodb-driver-manager.addsubscriber.html) - реєструє передплатника на подію моніторингу в даному об'єкті Manager
-   [Мониторинг производительности приложения (Application Performance Monitoring или APM)](mongodb.tutorial.apm.html)