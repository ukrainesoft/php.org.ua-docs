---
navigation:
  - class.mongodb-driver-monitoring-commandsubscriber.html: « MongoDBDriverMonitoringCommandSubscriber
  - mongodb-driver-monitoring-commandsubscriber.commandstarted.html: 'MongoDBDriverMonitoringCommandSubscriber::commandStarted »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-commandsubscriber.html: MongoDBDriverMonitoringCommandSubscriber
title: 'MongoDBDriverMonitoringCommandSubscriber::commandFailed'
---
# MongoDBDriverMonitoringCommandSubscriber::commandFailed

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandSubscriber::commandFailed — Метод сповіщення про невдалу команду

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\CommandSubscriber::commandFailed(MongoDB\Driver\Monitoring\CommandFailedEvent $event): void
```

Якщо передплатник зареєстровано, драйвер викличе цей метод у разі помилки команди.

### Список параметрів

`event` [MongoDBDriverMonitoringCommandFailedEvent](class.mongodb-driver-monitoring-commandfailedevent.html)

Об'єкт події, що містить інформацію про невдалу команду.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverMonitoringCommandFailedEvent](class.mongodb-driver-monitoring-commandfailedevent.html)
-   [MongoDBDriverMonitoringaddSubscriber()](function.mongodb.driver.monitoring.addsubscriber.md) - Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDBDriverManager::addSubscriber()](mongodb-driver-manager.addsubscriber.html) - реєструє передплатника на подію моніторингу в даному об'єкті Manager
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.md)
