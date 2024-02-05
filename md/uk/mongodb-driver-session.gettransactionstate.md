---
navigation:
  - mongodb-driver-session.gettransactionoptions.md: '« MongoDB\\Driver\\Session::getTransactionOptions'
  - mongodb-driver-session.isdirty.md: 'MongoDB\\Driver\\Session::isDirty »'
  - index.md: PHP Manual
  - class.mongodb-driver-session.md: MongoDB\\Driver\\Session
title: 'MongoDB\\Driver\\Session::getTransactionState'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Session::getTransactionState

(mongodb >=1.7.0)

MongoDB\\Driver\\Session::getTransactionState — Повертає статус транзакції для поточної сесії

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

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Session::isInTransaction()](mongodb-driver-session.isintransaction.md) \- Визначає, чи відбувається зараз багатодокументна транзакція
-   [MongoDB\\Driver\\Session::getTransactionOptions()](mongodb-driver-session.gettransactionoptions.md) \- Повертає налаштування поточної транзакції
