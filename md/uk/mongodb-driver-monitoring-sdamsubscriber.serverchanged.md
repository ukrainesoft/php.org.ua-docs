---
navigation:
  - class.mongodb-driver-monitoring-sdamsubscriber.md: « MongoDB\\Driver\\Monitoring\\SDAMSubscriber
  - mongodb-driver-monitoring-sdamsubscriber.serverclosed.md: 'MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverClosed »'
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-sdamsubscriber.md: MongoDB\\Driver\\Monitoring\\SDAMSubscriber
title: 'MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverChanged'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverChanged

(mongodb >=1.13.0)

MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverChanged — Метод сповіщення про зміну опису сервера

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\SDAMSubscriber::serverChanged(MongoDB\Driver\Monitoring\ServerChangedEvent $event): void
```

Якщо передплатник був зареєстрований, драйвер викликатиме цей метод, якщо опис сервера змінився.

### Список параметрів

`event` [MongoDB\\Driver\\Monitoring\\ServerChangedEvent](class.mongodb-driver-monitoring-serverchangedevent.md)) .

Об'єкт події, що містить інформацію про змінений опис сервера.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\ServerChangedEvent](class.mongodb-driver-monitoring-serverchangedevent.md)
-   [MongoDB\\Driver\\Monitoring\\addSubscriber()](function.mongodb.driver.monitoring.addsubscriber.md) \- Глобальна реєстрація передплатника на подію моніторингу
-   [MongoDB\\Driver\\Manager::addSubscriber()](mongodb-driver-manager.addsubscriber.md) \- реєструє передплатника на подію моніторингу в даному об'єкті Manager
