---
navigation:
  - mongodb-driver-session.getlogicalsessionid.md: '« MongoDB\\Driver\\Session::getLogicalSessionId'
  - mongodb-driver-session.getserver.md: 'MongoDB\\Driver\\Session::getServer »'
  - index.md: PHP Manual
  - class.mongodb-driver-session.md: MongoDB\\Driver\\Session
title: 'MongoDB\\Driver\\Session::getOperationTime'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Session::getOperationTime

(mongodb >=1.4.0)

MongoDB\\Driver\\Session::getOperationTime — Повертає час операції для цього сеансу

### Опис

```methodsynopsis
final public MongoDB\Driver\Session::getOperationTime(): ?MongoDB\BSON\Timestamp
```

Повертає час операції для цього сеансу. Якщо сеанс не використовувався для жодної операції, і [MongoDB\\Driver\\Session::advanceOperationTime()](mongodb-driver-session.advanceoperationtime.md) не був викликаний, час операції буде рівним **`null`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає час операції для цього сеансу або **`null`**, якщо сеанс не має часу операції.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Session::advanceOperationTime()](mongodb-driver-session.advanceoperationtime.md) \- Збільшує час операції для сеансу
