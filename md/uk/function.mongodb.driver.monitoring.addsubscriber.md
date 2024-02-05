---
navigation:
  - ref.monitoring.functions.md: « Функції
  - function.mongodb.driver.monitoring.removesubscriber.md: MongoDB\\Driver\\Monitoring\\removeSubscriber »
  - index.md: PHP Manual
  - ref.monitoring.functions.md: Функції
title: MongoDB\\Driver\\Monitoring\\addSubscriber
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\addSubscriber

(mongodb >=1.3.0)

MongoDB\\Driver\\Monitoring\\addSubscriber — Глобальна реєстрація передплатника на подію моніторингу

### Опис

```methodsynopsis
MongoDB\Driver\Monitoring\addSubscriber(MongoDB\Driver\Monitoring\Subscriber $subscriber): void
```

Глобально реєструє передплатника на подію моніторингу. Передплатник буде повідомлено про всі події драйвера для будь-якого менеджера.

> **Зауваження**: Якщо `subscriber` вже зареєстровано глобально, функція відпрацює без результату. Якщо `subscriber` також зареєстрований з одним або декількома менеджерами, він все одно отримає повідомлення один раз про кожну подію для кожного менеджера.

### Список параметрів

`subscriber` [MongoDB\\Driver\\Monitoring\\Subscriber](class.mongodb-driver-monitoring-subscriber.md)) .

Передплатник моніторингу подій для глобальної реєстрації.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\removeSubscriber()](function.mongodb.driver.monitoring.removesubscriber.md) \- скасовує глобальну реєстрацію передплатника на подію моніторингу
-   [MongoDB\\Driver\\Monitoring\\Subscriber](class.mongodb-driver-monitoring-subscriber.md)
-   [MongoDB\\Driver\\Monitoring\\CommandSubscriber](class.mongodb-driver-monitoring-commandsubscriber.md)
-   [MongoDB\\Driver\\Manager::addSubscriber()](mongodb-driver-manager.addsubscriber.md) \- реєструє передплатника на подію моніторингу в даному об'єкті Manager
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
