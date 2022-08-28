Скасує глобальну реєстрацію передплатника на подію моніторингу

-   [« MongoDB\\Driver\\Monitoring\\addSubscriber](function.mongodb.driver.monitoring.addsubscriber.html)
    
-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent »](class.mongodb-driver-monitoring-commandfailedevent.html)
    
-   [PHP Manual](index.html)
    
-   [Функции](ref.monitoring.functions.html)
    
-   Скасує глобальну реєстрацію передплатника на подію моніторингу
    

# MongoDBDriverMonitoringremoveSubscriber

(mongodb >=1.3.0)

MongoDBDriverMonitoringremoveSubscriber — Скасує глобальну реєстрацію передплатника на подію моніторингу

### Опис

```methodsynopsis
MongoDB\Driver\Monitoring\removeSubscriber(MongoDB\Driver\Monitoring\Subscriber $subscriber): void
```

Скасує глобальну реєстрацію передплатника на подію моніторингу.

> **Зауваження**: Якщо `subscriber` ще не зареєстровано глобально, функція відпрацює без результату.

### Список параметрів

`subscriber` [MongoDB\\Driver\\Monitoring\\Subscriber](class.mongodb-driver-monitoring-subscriber.html)

Передплатник на подію моніторингу для глобального скасування реєстрації.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\addSubscriber()](function.mongodb.driver.monitoring.addsubscriber.html) - Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDB\\Driver\\Monitoring\\Subscriber](class.mongodb-driver-monitoring-subscriber.html)
-   [MongoDB\\Driver\\Monitoring\\CommandSubscriber](class.mongodb-driver-monitoring-commandsubscriber.html)
-   [MongoDB\\Driver\\Manager::removeSubscriber()](mongodb-driver-manager.removesubscriber.html) - Скасує реєстрацію передплатника на подію моніторингу в даному об'єкті Manager
-   [Мониторинг производительности приложения (Application Performance Monitoring или APM)](mongodb.tutorial.apm.html)