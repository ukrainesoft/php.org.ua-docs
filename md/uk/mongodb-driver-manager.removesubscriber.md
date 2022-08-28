Скасує реєстрацію передплатника на подію моніторингу в даному об'єкті Manager

-   [« MongoDB\\Driver\\Manager::getWriteConcern](mongodb-driver-manager.getwriteconcern.html)
    
-   [MongoDB\\Driver\\Manager::selectServer »](mongodb-driver-manager.selectserver.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Manager](class.mongodb-driver-manager.html)
    
-   Скасує реєстрацію передплатника на подію моніторингу в даному об'єкті Manager
    

# MongoDBDriverManager::removeSubscriber

(mongodb >=1.10.0)

MongoDBDriverManager::removeSubscriber — Скасує реєстрацію передплатника на подію моніторингу в даному об'єкті Manager

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::removeSubscriber(MongoDB\Driver\Monitoring\Subscriber $subscriber): void
```

Скасує реєстрацію передплатника на подію моніторингу у цьому об'єкті Manager.

> **Зауваження**: Якщо `subscriber` ще не зареєстрований у цьому об'єкті Manager, функція відпрацює без результату.

### Список параметрів

`subscriber` [MongoDB\\Driver\\Monitoring\\Subscriber](class.mongodb-driver-monitoring-subscriber.html)

Передплатник на подію моніторингу, якому необхідно скасувати реєстрацію в об'єкті Manager.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Manager::addSubscriber()](mongodb-driver-manager.addsubscriber.html) - реєструє передплатника на подію моніторингу в даному об'єкті Manager
-   [MongoDB\\Driver\\Monitoring\\Subscriber](class.mongodb-driver-monitoring-subscriber.html)
-   [MongoDB\\Driver\\Monitoring\\CommandSubscriber](class.mongodb-driver-monitoring-commandsubscriber.html)
-   [MongoDB\\Driver\\Monitoring\\removeSubscriber()](function.mongodb.driver.monitoring.removesubscriber.html) - скасовує глобальну реєстрацію передплатника на подію моніторингу
-   [Мониторинг производительности приложения (Application Performance Monitoring или APM)](mongodb.tutorial.apm.html)