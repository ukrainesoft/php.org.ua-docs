---
navigation:
  - mongodb-driver-session.gettransactionstate.html: '« MongoDBDriverSession::getTransactionState'
  - mongodb-driver-session.isintransaction.html: 'MongoDBDriverSession::isInTransaction »'
  - index.html: PHP Manual
  - class.mongodb-driver-session.html: MongoDBDriverSession
title: 'MongoDBDriverSession::isDirty'
---
# MongoDBDriverSession::isDirty

(mongodb >=1.13.0)

MongoDBDriverSession::isDirty - Повертає, чи була сесія позначена як брудна

### Опис

```methodsynopsis
final public MongoDB\Driver\Session::isDirty(): bool
```

Повертає, чи була сесія позначена як брудна (тобто була використана з командою, яка зіткнулася з мережевою помилкою).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція повертає, чи сесія була позначена як брудна.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
