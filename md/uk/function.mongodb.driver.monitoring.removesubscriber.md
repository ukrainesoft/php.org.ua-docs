---
navigation:
  - function.mongodb.driver.monitoring.addsubscriber.md: « MongoDBDriverMonitoringaddSubscriber
  - class.mongodb-driver-monitoring-commandfailedevent.md: MongoDBDriverMonitoringCommandFailedEvent »
  - index.md: PHP Manual
  - ref.monitoring.functions.md: Функції
title: MongoDBDriverMonitoringremoveSubscriber
---
# MongoDBDriverMonitoringremoveSubscriber

(mongodb >=1.3.0)

MongoDBDriverMonitoringremoveSubscriber — Скасує глобальну реєстрацію передплатника на подію моніторингу

### Опис

```methodsynopsis
MongoDB\Driver\Monitoring\removeSubscriber(MongoDB\Driver\Monitoring\Subscriber $subscriber): void
```

Скасує глобальну реєстрацію передплатника на подію моніторингу.

> **Зауваження**: Якщо `subscriber` ще не зареєстровано глобально, функція відпрацює без результату.

### Список параметрів

`subscriber` [MongoDBDriverMonitoringSubscriber](class.mongodb-driver-monitoring-subscriber.md)

Передплатник на подію моніторингу для глобального скасування реєстрації.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverMonitoringaddSubscriber()](function.mongodb.driver.monitoring.addsubscriber.md) - Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDBDriverMonitoringSubscriber](class.mongodb-driver-monitoring-subscriber.md)
-   [MongoDBDriverMonitoringCommandSubscriber](class.mongodb-driver-monitoring-commandsubscriber.md)
-   [MongoDBDriverManager::removeSubscriber()](mongodb-driver-manager.removesubscriber.md) - Скасує реєстрацію передплатника на подію моніторингу в даному об'єкті Manager
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
