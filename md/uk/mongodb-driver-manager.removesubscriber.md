---
navigation:
  - mongodb-driver-manager.getwriteconcern.html: '« MongoDBDriverManager::getWriteConcern'
  - mongodb-driver-manager.selectserver.html: 'MongoDBDriverManager::selectServer »'
  - index.html: PHP Manual
  - class.mongodb-driver-manager.html: MongoDBDriverManager
title: 'MongoDBDriverManager::removeSubscriber'
---
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

`subscriber` [MongoDBDriverMonitoringSubscriber](class.mongodb-driver-monitoring-subscriber.html)

Передплатник на подію моніторингу, якому необхідно скасувати реєстрацію в об'єкті Manager.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverManager::addSubscriber()](mongodb-driver-manager.addsubscriber.html) - реєструє передплатника на подію моніторингу в даному об'єкті Manager
-   [MongoDBDriverMonitoringSubscriber](class.mongodb-driver-monitoring-subscriber.html)
-   [MongoDBDriverMonitoringCommandSubscriber](class.mongodb-driver-monitoring-commandsubscriber.html)
-   [MongoDBDriverMonitoringremoveSubscriber()](function.mongodb.driver.monitoring.removesubscriber.html) - скасовує глобальну реєстрацію передплатника на подію моніторингу
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.html)
