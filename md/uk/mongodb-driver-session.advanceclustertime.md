---
navigation:
  - mongodb-driver-session.aborttransaction.md: '« MongoDB\\Driver\\Session::abortTransaction'
  - mongodb-driver-session.advanceoperationtime.md: 'MongoDB\\Driver\\Session::advanceOperationTime »'
  - index.md: PHP Manual
  - class.mongodb-driver-session.md: MongoDB\\Driver\\Session
title: 'MongoDB\\Driver\\Session::advanceClusterTime'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Session::advanceClusterTime

(mongodb >=1.4.0)

MongoDB\\Driver\\Session::advanceClusterTime — Збільшує час кластера для сеансу

### Опис

```methodsynopsis
final public MongoDB\Driver\Session::advanceClusterTime(array|object $clusterTime): void
```

Підвищує час кластера для сеансу. Якщо час кластера менше або дорівнює поточному часу кластера сеансу, функція не працюватиме.

Використовуючи цей метод у поєднанні з [MongoDB\\Driver\\Session::advanceOperationTime()](mongodb-driver-session.advanceoperationtime.md) Для копіювання кластера та часу операцій з іншого сеансу, ви можете переконатися, що операції на цьому сеансі причинно відповідають останній операції в іншому сеансі.

### Список параметрів

`clusterTime`

Час кластера - це документ, що містить логічну мітку часу та сигнатуру сервера. Як правило, це значення буде отримано шляхом виклику [MongoDB\\Driver\\Session::getClusterTime()](mongodb-driver-session.getclustertime.md) для іншого об'єкта сеансу.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Session::advanceOperationTime()](mongodb-driver-session.advanceoperationtime.md) \- Збільшує час операції для сеансу
-   [MongoDB\\Driver\\Session::getClusterTime()](mongodb-driver-session.getclustertime.md) \- Повертає час кластера для цього сеансу
