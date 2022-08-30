Метод повідомлення про запущену команду

-   [« MongoDBDriverMonitoringCommandSubscriber::commandFailed](mongodb-driver-monitoring-commandsubscriber.commandfailed.html)
    
-   [MongoDBDriverMonitoringCommandSubscriber::commandSucceeded »](mongodb-driver-monitoring-commandsubscriber.commandsucceeded.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverMonitoringCommandSubscriber](class.mongodb-driver-monitoring-commandsubscriber.html)
    
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

`event` [MongoDBDriverMonitoringCommandStartedEvent](class.mongodb-driver-monitoring-commandstartedevent.html)

Об'єкт події, що містить інформацію про запущену команду.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverMonitoringCommandStartedEvent](class.mongodb-driver-monitoring-commandstartedevent.html)
-   [MongoDBDriverMonitoringaddSubscriber()](function.mongodb.driver.monitoring.addsubscriber.html) - Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDBDriverManager::addSubscriber()](mongodb-driver-manager.addsubscriber.html) - реєструє передплатника на подію моніторингу в даному об'єкті Manager
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.html)