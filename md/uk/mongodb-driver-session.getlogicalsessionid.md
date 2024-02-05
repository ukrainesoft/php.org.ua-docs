---
navigation:
  - mongodb-driver-session.getclustertime.md: '« MongoDB\\Driver\\Session::getClusterTime'
  - mongodb-driver-session.getoperationtime.md: 'MongoDB\\Driver\\Session::getOperationTime »'
  - index.md: PHP Manual
  - class.mongodb-driver-session.md: MongoDB\\Driver\\Session
title: 'MongoDB\\Driver\\Session::getLogicalSessionId'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Session::getLogicalSessionId

(mongodb >=1.4.0)

MongoDB\\Driver\\Session::getLogicalSessionId — Повертає логічний ідентифікатор сеансу для цього сеансу

### Опис

```methodsynopsis
final public MongoDB\Driver\Session::getLogicalSessionId(): object
```

Повертає логічний ідентифікатор сеансу для цього сеансу, який можна використовувати для ідентифікації операцій сеансу на сервері.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає логічний ідентифікатор сеансу цього сеансу.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
