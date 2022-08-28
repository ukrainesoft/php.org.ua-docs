Метод повідомлення про невдалу команду

-   [« MongoDB\\Driver\\Monitoring\\CommandSubscriber](class.mongodb-driver-monitoring-commandsubscriber.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandStarted »](mongodb-driver-monitoring-commandsubscriber.commandstarted.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandSubscriber](class.mongodb-driver-monitoring-commandsubscriber.html)
    
-   Метод повідомлення про невдалу команду
    

# MongoDBDriverMonitoringCommandSubscriber::commandFailed

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandSubscriber::commandFailed — Метод сповіщення про невдалу команду

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\CommandSubscriber::commandFailed(MongoDB\Driver\Monitoring\CommandFailedEvent $event): void
```

Якщо передплатник зареєстровано, драйвер викличе цей метод у разі помилки команди.

### Список параметрів

`event` [MongoDB\\Driver\\Monitoring\\CommandFailedEvent](class.mongodb-driver-monitoring-commandfailedevent.html)

Об'єкт події, що містить інформацію про невдалу команду.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent](class.mongodb-driver-monitoring-commandfailedevent.html)
-   [MongoDB\\Driver\\Monitoring\\addSubscriber()](function.mongodb.driver.monitoring.addsubscriber.html) - Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDB\\Driver\\Manager::addSubscriber()](mongodb-driver-manager.addsubscriber.html) - реєструє передплатника на подію моніторингу в даному об'єкті Manager
-   [Мониторинг производительности приложения (Application Performance Monitoring или APM)](mongodb.tutorial.apm.html)