Реєструє передплатника на подію моніторингу в даному об'єкті Manager

-   [« MongoDB\\Driver\\Manager](class.mongodb-driver-manager.html)
    
-   [MongoDB\\Driver\\Manager::\_\_construct »](mongodb-driver-manager.construct.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Manager](class.mongodb-driver-manager.html)
    
-   Реєструє передплатника на подію моніторингу в даному об'єкті Manager
    

# MongoDBDriverManager::addSubscriber

(mongodb >=1.10.0)

MongoDBDriverManager::addSubscriber — Зареєструє передплатника на подію моніторингу в даному об'єкті Manager

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::addSubscriber(MongoDB\Driver\Monitoring\Subscriber $subscriber): void
```

Реєструє передплатника на подію моніторингу у цьому об'єкті Manager. Передплатник буде повідомлено про всі події цього об'єкта Manager.

> **Зауваження**: Якщо `subscriber` вже зареєстровано в цьому об'єкті Manager, ця функція буде недоступною. Якщо `subscriber` також зареєстрований глобально, він все одно отримуватиме повідомлення лише один раз про кожну подію для цього об'єкта Manager.

### Список параметрів

`subscriber` [MongoDB\\Driver\\Monitoring\\Subscriber](class.mongodb-driver-monitoring-subscriber.html)

Передплатник подій моніторингу, який має бути зареєстрований у цьому об'єкті Manager.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Manager::removeSubscriber()](mongodb-driver-manager.removesubscriber.html) - Скасує реєстрацію передплатника на подію моніторингу в даному об'єкті Manager
-   [MongoDB\\Driver\\Monitoring\\Subscriber](class.mongodb-driver-monitoring-subscriber.html)
-   [MongoDB\\Driver\\Monitoring\\CommandSubscriber](class.mongodb-driver-monitoring-commandsubscriber.html)
-   [MongoDB\\Driver\\Monitoring\\addSubscriber()](function.mongodb.driver.monitoring.addsubscriber.html) - Глобальна реєстрація передплатника на подію моніторингу
-   [Мониторинг производительности приложения (Application Performance Monitoring или APM)](mongodb.tutorial.apm.html)