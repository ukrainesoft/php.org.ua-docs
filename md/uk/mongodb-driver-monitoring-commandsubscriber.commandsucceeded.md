---
navigation:
  - mongodb-driver-monitoring-commandsubscriber.commandstarted.html: '« MongoDBDriverMonitoringCommandSubscriber::commandStarted'
  - class.mongodb-driver-monitoring-sdamsubscriber.html: MongoDBDriverMonitoringSDAMSubscriber »
  - index.html: PHP Manual
  - class.mongodb-driver-monitoring-commandsubscriber.html: MongoDBDriverMonitoringCommandSubscriber
title: 'MongoDBDriverMonitoringCommandSubscriber::commandSucceeded'
---
# MongoDBDriverMonitoringCommandSubscriber::commandSucceeded

(mongodb >=1.3.0)

MongoDBDriverMonitoringCommandSubscriber::commandSucceeded — Метод сповіщення про успішну команду

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\CommandSubscriber::commandSucceeded(MongoDB\Driver\Monitoring\CommandSucceededEvent $event): void
```

Якщо передплатник зареєстровано, драйвер викличе цей метод у разі успішного виконання команди.

### Список параметрів

`event` [MongoDBDriverMonitoringCommandSucceededEvent](class.mongodb-driver-monitoring-commandsucceededevent.html)

Об'єкт події, що містить інформацію про успішну команду.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverMonitoringCommandSucceededEvent](class.mongodb-driver-monitoring-commandsucceededevent.html)
-   [MongoDBDriverMonitoringaddSubscriber()](function.mongodb.driver.monitoring.addsubscriber.html) - Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDBDriverManager::addSubscriber()](mongodb-driver-manager.addsubscriber.html) - реєструє передплатника на подію моніторингу в даному об'єкті Manager
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.html)
