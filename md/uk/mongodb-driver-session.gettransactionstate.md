---
navigation:
  - mongodb-driver-session.gettransactionoptions.html: '« MongoDBDriverSession::getTransactionOptions'
  - mongodb-driver-session.isdirty.html: 'MongoDBDriverSession::isDirty »'
  - index.html: PHP Manual
  - class.mongodb-driver-session.html: MongoDBDriverSession
title: 'MongoDBDriverSession::getTransactionState'
---
# MongoDBDriverSession::getTransactionState

(mongodb >=1.7.0)

MongoDBDriverSession::getTransactionState — Повертає статус транзакції для поточної сесії

### Опис

```methodsynopsis
final public MongoDB\Driver\Session::getTransactionState(): string
```

Повертає статус транзакції для сесії.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає статус транзакції для сесії.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverSession::isInTransaction()](mongodb-driver-session.isintransaction.html) - Визначає, чи відбувається зараз багатодокументна транзакція
-   [MongoDBDriverSession::getTransactionOptions()](mongodb-driver-session.gettransactionoptions.html) - Повертає налаштування поточної транзакції
