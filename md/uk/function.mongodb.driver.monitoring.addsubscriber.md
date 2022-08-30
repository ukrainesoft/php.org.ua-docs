Глобальна реєстрація передплатника на подію моніторингу

-   [« Функції](ref.monitoring.functions.html)
    
-   [MongoDBDriverMonitoringremoveSubscriber »](function.mongodb.driver.monitoring.removesubscriber.html)
    
-   [PHP Manual](index.html)
    
-   [Функції](ref.monitoring.functions.html)
    
-   Глобальна реєстрація передплатника на подію моніторингу
    

# MongoDBDriverMonitoringaddSubscriber

(mongodb >=1.3.0)

MongoDBDriverMonitoringaddSubscriber — Глобальна реєстрація передплатника на подію моніторингу

### Опис

```methodsynopsis
MongoDB\Driver\Monitoring\addSubscriber(MongoDB\Driver\Monitoring\Subscriber $subscriber): void
```

Глобально реєструє передплатника на подію моніторингу. Передплатник буде повідомлено про всі події драйвера для будь-якого менеджера.

> **Зауваження**: Якщо `subscriber` вже зареєстровано глобально, функція відпрацює без результату. Якщо `subscriber` також зареєстрований з одним або декількома менеджерами, він все одно отримає повідомлення один раз про кожну подію для кожного менеджера.

### Список параметрів

`subscriber` [MongoDBDriverMonitoringSubscriber](class.mongodb-driver-monitoring-subscriber.html)

Передплатник моніторингу подій для глобальної реєстрації.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverMonitoringremoveSubscriber()](function.mongodb.driver.monitoring.removesubscriber.html) - скасовує глобальну реєстрацію передплатника на подію моніторингу
-   [MongoDBDriverMonitoringSubscriber](class.mongodb-driver-monitoring-subscriber.html)
-   [MongoDBDriverMonitoringCommandSubscriber](class.mongodb-driver-monitoring-commandsubscriber.html)
-   [MongoDBDriverManager::addSubscriber()](mongodb-driver-manager.addsubscriber.html) - реєструє передплатника на подію моніторингу в даному об'єкті Manager
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.html)