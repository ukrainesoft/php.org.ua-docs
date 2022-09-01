---
navigation:
  - class.mongodb-driver-monitoring-sdamsubscriber.html: « MongoDBDriverMonitoringSDAMSubscriber
  - mongodb-driver-monitoring-sdamsubscriber.serverclosed.html: 'MongoDBDriverMonitoringSDAMSubscriber::serverClosed »'
  - index.html: PHP Manual
  - class.mongodb-driver-monitoring-sdamsubscriber.html: MongoDBDriverMonitoringSDAMSubscriber
title: 'MongoDBDriverMonitoringSDAMSubscriber::serverChanged'
---
# MongoDBDriverMonitoringSDAMSubscriber::serverChanged

(mongodb >=1.13.0)

MongoDBDriverMonitoringSDAMSubscriber::serverChanged — Метод сповіщення про зміну опису сервера

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\SDAMSubscriber::serverChanged(MongoDB\Driver\Monitoring\ServerChangedEvent $event): void
```

Якщо передплатник був зареєстрований, драйвер викликатиме цей метод, якщо опис сервера змінився.

### Список параметрів

`event` [MongoDBDriverMonitoringServerChangedEvent](class.mongodb-driver-monitoring-serverchangedevent.html)

Об'єкт події, що містить інформацію про змінений опис сервера.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverMonitoringServerChangedEvent](class.mongodb-driver-monitoring-serverchangedevent.html)
-   [MongoDBDriverMonitoringaddSubscriber()](function.mongodb.driver.monitoring.addsubscriber.html) - Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDBDriverManager::addSubscriber()](mongodb-driver-manager.addsubscriber.html) - реєструє передплатника на подію моніторингу в даному об'єкті Manager
