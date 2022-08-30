Скасує глобальну реєстрацію передплатника на подію моніторингу

-   [« MongoDBDriverMonitoringaddSubscriber](function.mongodb.driver.monitoring.addsubscriber.html)
    
-   [MongoDBDriverMonitoringCommandFailedEvent »](class.mongodb-driver-monitoring-commandfailedevent.html)
    
-   [PHP Manual](index.html)
    
-   [Функції](ref.monitoring.functions.html)
    
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

`subscriber` [MongoDBDriverMonitoringSubscriber](class.mongodb-driver-monitoring-subscriber.html)

Передплатник на подію моніторингу для глобального скасування реєстрації.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverMonitoringaddSubscriber()](function.mongodb.driver.monitoring.addsubscriber.html) - Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDBDriverMonitoringSubscriber](class.mongodb-driver-monitoring-subscriber.html)
-   [MongoDBDriverMonitoringCommandSubscriber](class.mongodb-driver-monitoring-commandsubscriber.html)
-   [MongoDBDriverManager::removeSubscriber()](mongodb-driver-manager.removesubscriber.html) - Скасує реєстрацію передплатника на подію моніторингу в даному об'єкті Manager
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.html)