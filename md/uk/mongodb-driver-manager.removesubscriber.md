---
navigation:
  - mongodb-driver-manager.getwriteconcern.md: '« MongoDBDriverManager::getWriteConcern'
  - mongodb-driver-manager.selectserver.md: 'MongoDBDriverManager::selectServer »'
  - index.md: PHP Manual
  - class.mongodb-driver-manager.md: MongoDBDriverManager
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

`subscriber` [MongoDBDriverMonitoringSubscriber](class.mongodb-driver-monitoring-subscriber.md)

Передплатник на подію моніторингу, якому необхідно скасувати реєстрацію в об'єкті Manager.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverManager::addSubscriber()](mongodb-driver-manager.addsubscriber.md) - реєструє передплатника на подію моніторингу в даному об'єкті Manager
-   [MongoDBDriverMonitoringSubscriber](class.mongodb-driver-monitoring-subscriber.md)
-   [MongoDBDriverMonitoringCommandSubscriber](class.mongodb-driver-monitoring-commandsubscriber.md)
-   [MongoDBDriverMonitoringremoveSubscriber()](function.mongodb.driver.monitoring.removesubscriber.md) - скасовує глобальну реєстрацію передплатника на подію моніторингу
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
