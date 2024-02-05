---
navigation:
  - function.mongodb.driver.monitoring.addsubscriber.md: « MongoDB\\Driver\\Monitoring\\addSubscriber
  - class.mongodb-driver-monitoring-commandfailedevent.md: MongoDB\\Driver\\Monitoring\\CommandFailedEvent »
  - index.md: PHP Manual
  - ref.monitoring.functions.md: Функції
title: MongoDB\\Driver\\Monitoring\\removeSubscriber
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\removeSubscriber

(mongodb >=1.3.0)

MongoDB\\Driver\\Monitoring\\removeSubscriber — Скасує глобальну реєстрацію передплатника на подію моніторингу

### Опис

```methodsynopsis
MongoDB\Driver\Monitoring\removeSubscriber(MongoDB\Driver\Monitoring\Subscriber $subscriber): void
```

Скасує глобальну реєстрацію передплатника на подію моніторингу.

> **Зауваження**: Якщо `subscriber` ще не зареєстровано глобально, функція відпрацює без результату.

### Список параметрів

`subscriber` [MongoDB\\Driver\\Monitoring\\Subscriber](class.mongodb-driver-monitoring-subscriber.md)) .

Передплатник на подію моніторингу для глобального скасування реєстрації.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\addSubscriber()](function.mongodb.driver.monitoring.addsubscriber.md) \- Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDB\\Driver\\Monitoring\\Subscriber](class.mongodb-driver-monitoring-subscriber.md)
-   [MongoDB\\Driver\\Monitoring\\CommandSubscriber](class.mongodb-driver-monitoring-commandsubscriber.md)
-   [MongoDB\\Driver\\Manager::removeSubscriber()](mongodb-driver-manager.removesubscriber.md) \- Скасує реєстрацію передплатника на подію моніторингу в даному об'єкті Manager
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
