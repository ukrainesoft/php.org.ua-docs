---
navigation:
  - mongodb-driver-session.committransaction.md: '« MongoDB\\Driver\\Session::commitTransaction'
  - mongodb-driver-session.endsession.md: 'MongoDB\\Driver\\Session::endSession »'
  - index.md: PHP Manual
  - class.mongodb-driver-session.md: MongoDB\\Driver\\Session
title: 'MongoDB\\Driver\\Session::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Session::\_\_construct

(mongodb >=1.4.0)

MongoDB\\Driver\\Session::\_\_construct — Створення нового сеансу (не використовується)

### Опис

```methodsynopsis
final private MongoDB\Driver\Session::__construct()
```

[MongoDB\\Driver\\Session](class.mongodb-driver-session.md) об'єкти повертаються [MongoDB\\Driver\\Manager::startSession()](mongodb-driver-manager.startsession.md) і не можуть бути створені безпосередньо.

### Список параметрів

Ця функція не має параметрів.

### Дивіться також

-   [MongoDB\\Driver\\Manager::startSession()](mongodb-driver-manager.startsession.md) \- Запускає новий сеанс клієнта для використання з цим клієнтом
