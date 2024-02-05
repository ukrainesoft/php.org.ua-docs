---
navigation:
  - mongodb-driver-manager.getwriteconcern.md: '« MongoDB\\Driver\\Manager::getWriteConcern'
  - mongodb-driver-manager.selectserver.md: 'MongoDB\\Driver\\Manager::selectServer »'
  - index.md: PHP Manual
  - class.mongodb-driver-manager.md: MongoDB\\Driver\\Manager
title: 'MongoDB\\Driver\\Manager::removeSubscriber'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Manager::removeSubscriber

(mongodb >=1.10.0)

MongoDB\\Driver\\Manager::removeSubscriber — Скасує реєстрацію передплатника на подію моніторингу в даному об'єкті Manager

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::removeSubscriber(MongoDB\Driver\Monitoring\Subscriber $subscriber): void
```

Скасує реєстрацію передплатника на подію моніторингу у цьому об'єкті Manager.

> **Зауваження**: Якщо `subscriber` ще не зареєстрований у цьому об'єкті Manager, функція відпрацює без результату.

### Список параметрів

`subscriber` [MongoDB\\Driver\\Monitoring\\Subscriber](class.mongodb-driver-monitoring-subscriber.md)) .

Передплатник на подію моніторингу, якому необхідно скасувати реєстрацію в об'єкті Manager.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Manager::addSubscriber()](mongodb-driver-manager.addsubscriber.md) \- реєструє передплатника на подію моніторингу в даному об'єкті Manager
-   [MongoDB\\Driver\\Monitoring\\Subscriber](class.mongodb-driver-monitoring-subscriber.md)
-   [MongoDB\\Driver\\Monitoring\\CommandSubscriber](class.mongodb-driver-monitoring-commandsubscriber.md)
-   [MongoDB\\Driver\\Monitoring\\removeSubscriber()](function.mongodb.driver.monitoring.removesubscriber.md) \- скасовує глобальну реєстрацію передплатника на подію моніторингу
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
