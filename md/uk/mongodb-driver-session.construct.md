---
navigation:
  - mongodb-driver-session.committransaction.md: '« MongoDBDriverSession::commitTransaction'
  - mongodb-driver-session.endsession.md: 'MongoDBDriverSession::endSession »'
  - index.md: PHP Manual
  - class.mongodb-driver-session.md: MongoDBDriverSession
title: 'MongoDBDriverSession::construct'
---
# MongoDBDriverSession::construct

(mongodb >=1.4.0)

MongoDBDriverSession::construct — Створення нового сеансу (не використовується)

### Опис

```methodsynopsis
final private MongoDB\Driver\Session::__construct()
```

[MongoDBDriverSession](class.mongodb-driver-session.md) об'єкти повертаються [MongoDBDriverManager::startSession()](mongodb-driver-manager.startsession.md) і не можуть бути створені безпосередньо.

### Список параметрів

Ця функція не має параметрів.

### Дивіться також

-   [MongoDBDriverManager::startSession()](mongodb-driver-manager.startsession.md) - Запуск нового клієнтського сеансу для використання з цим клієнтом
