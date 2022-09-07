---
navigation:
  - mongodb-driver-session.endsession.md: '« MongoDBDriverSession::endSession'
  - mongodb-driver-session.getlogicalsessionid.md: 'MongoDBDriverSession::getLogicalSessionId »'
  - index.md: PHP Manual
  - class.mongodb-driver-session.md: MongoDBDriverSession
title: 'MongoDBDriverSession::getClusterTime'
---
# MongoDBDriverSession::getClusterTime

(mongodb >=1.4.0)

MongoDBDriverSession::getClusterTime — Повертає час кластера для цього сеансу

### Опис

```methodsynopsis
final public MongoDB\Driver\Session::getClusterTime(): ?object
```

Повертає час кластера для цього сеансу. Якщо сеанс не використовувався для будь-якої операції та [MongoDBDriverSession::advanceClusterTime()](mongodb-driver-session.advanceclustertime.md) не був викликаний, час кластера буде рівний **`null`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає час кластера для цього сеансу або **`null`**, якщо сеанс не має часу кластера.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverSession::advanceClusterTime()](mongodb-driver-session.advanceclustertime.md) - Збільшує час кластера для сеансу
