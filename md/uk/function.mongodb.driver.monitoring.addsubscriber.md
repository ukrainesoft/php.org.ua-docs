Глобальна реєстрація передплатника на подію моніторингу

-   [« Функции](ref.monitoring.functions.html)
    
-   [MongoDB\\Driver\\Monitoring\\removeSubscriber »](function.mongodb.driver.monitoring.removesubscriber.html)
    
-   [PHP Manual](index.html)
    
-   [Функции](ref.monitoring.functions.html)
    
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

`subscriber` [MongoDB\\Driver\\Monitoring\\Subscriber](class.mongodb-driver-monitoring-subscriber.html)

Передплатник моніторингу подій для глобальної реєстрації.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\removeSubscriber()](function.mongodb.driver.monitoring.removesubscriber.html) - скасовує глобальну реєстрацію передплатника на подію моніторингу
-   [MongoDB\\Driver\\Monitoring\\Subscriber](class.mongodb-driver-monitoring-subscriber.html)
-   [MongoDB\\Driver\\Monitoring\\CommandSubscriber](class.mongodb-driver-monitoring-commandsubscriber.html)
-   [MongoDB\\Driver\\Manager::addSubscriber()](mongodb-driver-manager.addsubscriber.html) - реєструє передплатника на подію моніторингу в даному об'єкті Manager
-   [Мониторинг производительности приложения (Application Performance Monitoring или APM)](mongodb.tutorial.apm.html)