---
navigation:
  - mongodb-driver-monitoring-commandsubscriber.commandfailed.html: '« MongoDBDriverMonitoringCommandSubscriber::commandFailed'
  - mongodb-driver-monitoring-commandsubscriber.commandsucceeded.html: 'MongoDBDriverMonitoringCommandSubscriber::commandSucceeded »'
  - index.html: PHP Manual
  - class.mongodb-driver-monitoring-commandsubscriber.html: MongoDBDriverMonitoringCommandSubscriber
title: 'MongoDBDriverMonitoringCommandSubscriber::commandStarted'
---
# MongoDBDriverMonitoringCommandSubscriber::commandStarted

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandSubscriber::commandStarted — Метод сповіщення про запущену команду

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\CommandSubscriber::commandStarted(MongoDB\Driver\Monitoring\CommandStartedEvent $event): void
```

Якщо передплатник зареєстровано, драйвер викличе цей метод під час запуску команди.

### Список параметрів

`event` [MongoDBDriverMonitoringCommandStartedEvent](class.mongodb-driver-monitoring-commandstartedevent.md)

Об'єкт події, що містить інформацію про запущену команду.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverMonitoringCommandStartedEvent](class.mongodb-driver-monitoring-commandstartedevent.md)
-   [MongoDBDriverMonitoringaddSubscriber()](function.mongodb.driver.monitoring.addsubscriber.md) - Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDBDriverManager::addSubscriber()](mongodb-driver-manager.addsubscriber.md) - реєструє передплатника на подію моніторингу в даному об'єкті Manager
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
