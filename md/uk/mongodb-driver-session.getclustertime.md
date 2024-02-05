---
navigation:
  - mongodb-driver-session.endsession.md: '« MongoDB\\Driver\\Session::endSession'
  - mongodb-driver-session.getlogicalsessionid.md: 'MongoDB\\Driver\\Session::getLogicalSessionId »'
  - index.md: PHP Manual
  - class.mongodb-driver-session.md: MongoDB\\Driver\\Session
title: 'MongoDB\\Driver\\Session::getClusterTime'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Session::getClusterTime

(mongodb >=1.4.0)

MongoDB\\Driver\\Session::getClusterTime — Повертає час кластера для цього сеансу

### Опис

```methodsynopsis
final public MongoDB\Driver\Session::getClusterTime(): ?object
```

Повертає час кластера для цього сеансу. Якщо сеанс не використовувався для будь-якої операції та [MongoDB\\Driver\\Session::advanceClusterTime()](mongodb-driver-session.advanceclustertime.md) не був викликаний, час кластера буде рівний **`null`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає час кластера для цього сеансу або **`null`**, якщо сеанс не має часу кластера.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Session::advanceClusterTime()](mongodb-driver-session.advanceclustertime.md) \- Збільшує час кластера для сеансу
