---
navigation:
  - class.mongodb-driver-monitoring-logsubscriber.md: « MongoDB\\Driver\\Monitoring\\LogSubscriber
  - class.mongodb-driver-monitoring-sdamsubscriber.md: MongoDB\\Driver\\Monitoring\\SDAMSubscriber »
  - index.md: PHP Manual
  - class.mongodb-driver-monitoring-logsubscriber.md: MongoDB\\Driver\\Monitoring\\LogSubscriber
title: 'MongoDB\\Driver\\Monitoring\\LogSubscriber::log'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Monitoring\\LogSubscriber::log

(mongodb >=1.17.0)

MongoDB\\Driver\\Monitoring\\LogSubscriber::log — Метод сповіщення для журналу

### Опис

```methodsynopsis
abstract public MongoDB\Driver\Monitoring\LogSubscriber::log(int $level, string $domain, string $message): void
```

Якщо передплатник зареєстровано, драйвер викликатиме цей метод для кожного зареєстрованого повідомлення.

### Список параметрів

`level`

Уровень серьезности. Одна из[констант інтерфейсу](class.mongodb-driver-monitoring-logsubscriber.md#mongodb-driver-monitoring-logsubscriber.constants)

`domain`

Назву компонента драйвера, який вивів повідомлення журналу.

`message`

Повідомлення журналу.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Monitoring\\addSubscriber()](function.mongodb.driver.monitoring.addsubscriber.md) \- Глобальна реєстрація передплатника на подію моніторингу
