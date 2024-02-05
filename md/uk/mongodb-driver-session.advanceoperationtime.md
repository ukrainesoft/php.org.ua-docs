---
navigation:
  - mongodb-driver-session.advanceclustertime.md: '« MongoDB\\Driver\\Session::advanceClusterTime'
  - mongodb-driver-session.committransaction.md: 'MongoDB\\Driver\\Session::commitTransaction »'
  - index.md: PHP Manual
  - class.mongodb-driver-session.md: MongoDB\\Driver\\Session
title: 'MongoDB\\Driver\\Session::advanceOperationTime'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Session::advanceOperationTime

(mongodb >=1.4.0)

MongoDB\\Driver\\Session::advanceOperationTime — Збільшує час операції для сеансу

### Опис

```methodsynopsis
final public MongoDB\Driver\Session::advanceOperationTime(MongoDB\BSON\TimestampInterface $operationTime): void
```

Збільшує час операції для сеансу. Якщо час операції менше або дорівнює поточному часу сеансу, функція не працюватиме.

Використовуючи цей метод у поєднанні з [MongoDB\\Driver\\Session::advanceClusterTime()](mongodb-driver-session.advanceclustertime.md) Для копіювання операції та часу кластеризації з іншого сеансу, ви можете гарантувати, що операції у цьому сеансі причинно узгоджуються з останньою операцією на іншому сеансі.

### Список параметрів

`operationTime`

Час операції є логічною відміткою часу. Як правило, це значення буде отримано шляхом виклику [MongoDB\\Driver\\Session::getOperationTime()](mongodb-driver-session.getoperationtime.md) для іншого об'єкта сеансу.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Session::advanceClusterTime()](mongodb-driver-session.advanceclustertime.md) \- Збільшує час кластера для сеансу
-   [MongoDB\\Driver\\Session::getClusterTime()](mongodb-driver-session.getclustertime.md) \- Повертає час кластера для цього сеансу
