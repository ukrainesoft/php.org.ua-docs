---
navigation:
  - class.mongodb-driver-manager.md: « MongoDB\\Driver\\Manager
  - mongodb-driver-manager.construct.md: 'MongoDB\\Driver\\Manager::\_\_construct »'
  - index.md: PHP Manual
  - class.mongodb-driver-manager.md: MongoDB\\Driver\\Manager
title: 'MongoDB\\Driver\\Manager::addSubscriber'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Manager::addSubscriber

(mongodb >=1.10.0)

MongoDB\\Driver\\Manager::addSubscriber — Зареєструє передплатника на подію моніторингу в даному об'єкті Manager

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::addSubscriber(MongoDB\Driver\Monitoring\Subscriber $subscriber): void
```

Реєструє передплатника на подію моніторингу у цьому об'єкті Manager. Передплатник буде повідомлено про всі події цього об'єкта Manager.

> **Зауваження**: Якщо `subscriber` вже зареєстровано в цьому об'єкті Manager, ця функція буде недоступною. Якщо `subscriber` також зареєстрований глобально, він все одно отримуватиме повідомлення лише один раз про кожну подію для цього об'єкта Manager.

### Список параметрів

`subscriber` [MongoDB\\Driver\\Monitoring\\Subscriber](class.mongodb-driver-monitoring-subscriber.md)) .

Передплатник подій моніторингу, який має бути зареєстрований у цьому об'єкті Manager.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Викидається виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md), якщо `subscriber`является[MongoDB\\Driver\\Monitoring\\LogSubscriber](class.mongodb-driver-monitoring-logsubscriber.md), оскільки реєстратори можуть бути зареєстровані лише глобально.

### Дивіться також

-   [MongoDB\\Driver\\Manager::removeSubscriber()](mongodb-driver-manager.removesubscriber.md) \- Скасує реєстрацію передплатника на подію моніторингу в даному об'єкті Manager
-   [MongoDB\\Driver\\Monitoring\\Subscriber](class.mongodb-driver-monitoring-subscriber.md)
-   [MongoDB\\Driver\\Monitoring\\CommandSubscriber](class.mongodb-driver-monitoring-commandsubscriber.md)
-   [MongoDB\\Driver\\Monitoring\\addSubscriber()](function.mongodb.driver.monitoring.addsubscriber.md) \- Глобальна реєстрація передплатника на подію моніторингу
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
