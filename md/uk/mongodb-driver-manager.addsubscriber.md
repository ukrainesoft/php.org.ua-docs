---
navigation:
  - class.mongodb-driver-manager.html: « MongoDBDriverManager
  - mongodb-driver-manager.construct.html: 'MongoDBDriverManager::construct »'
  - index.md: PHP Manual
  - class.mongodb-driver-manager.html: MongoDBDriverManager
title: 'MongoDBDriverManager::addSubscriber'
---
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

`subscriber` [MongoDBDriverMonitoringSubscriber](class.mongodb-driver-monitoring-subscriber.md)

Передплатник подій моніторингу, який має бути зареєстрований у цьому об'єкті Manager.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverManager::removeSubscriber()](mongodb-driver-manager.removesubscriber.md) - Скасує реєстрацію передплатника на подію моніторингу в даному об'єкті Manager
-   [MongoDBDriverMonitoringSubscriber](class.mongodb-driver-monitoring-subscriber.md)
-   [MongoDBDriverMonitoringCommandSubscriber](class.mongodb-driver-monitoring-commandsubscriber.md)
-   [MongoDBDriverMonitoringaddSubscriber()](function.mongodb.driver.monitoring.addsubscriber.md) - Глобальна реєстрація передплатника на подію моніторингу
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
