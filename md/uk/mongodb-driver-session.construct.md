---
navigation:
  - mongodb-driver-session.committransaction.html: '« MongoDBDriverSession::commitTransaction'
  - mongodb-driver-session.endsession.html: 'MongoDBDriverSession::endSession »'
  - index.md: PHP Manual
  - class.mongodb-driver-session.html: MongoDBDriverSession
title: 'MongoDBDriverSession::construct'
---
# MongoDBDriverSession::construct

(mongodb >=1.4.0)

MongoDBDriverSession::construct — Створення нового сеансу (не використовується)

### Опис

```methodsynopsis
final private MongoDB\Driver\Session::__construct()
```

[MongoDBDriverSession](class.mongodb-driver-session.html) об'єкти повертаються [MongoDBDriverManager::startSession()](mongodb-driver-manager.startsession.md) і не можуть бути створені безпосередньо.

### Список параметрів

Ця функція не має параметрів.

### Дивіться також

-   [MongoDBDriverManager::startSession()](mongodb-driver-manager.startsession.md) - Запуск нового клієнтського сеансу для використання з цим клієнтом
