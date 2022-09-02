---
navigation:
  - mongodb-driver-session.getserver.md: '« MongoDBDriverSession::getServer'
  - mongodb-driver-session.gettransactionstate.md: 'MongoDBDriverSession::getTransactionState »'
  - index.md: PHP Manual
  - class.mongodb-driver-session.md: MongoDBDriverSession
title: 'MongoDBDriverSession::getTransactionOptions'
---
# MongoDBDriverSession::getTransactionOptions

(mongodb >=1.7.0)

MongoDBDriverSession::getTransactionOptions — Повертає установки поточної транзакції

### Опис

```methodsynopsis
final public MongoDB\Driver\Session::getTransactionOptions(): ?array
```

Повертає установки поточної транзакції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив, що містить налаштування поточної транзакції, або \*\*`null`\*\*якщо транзакція не стартована.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverSession::getTransactionState()](mongodb-driver-session.gettransactionstate.md) - Повертає статус транзакції для поточної сесії
