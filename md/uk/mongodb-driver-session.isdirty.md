---
navigation:
  - mongodb-driver-session.gettransactionstate.md: '« MongoDB\\Driver\\Session::getTransactionState'
  - mongodb-driver-session.isintransaction.md: 'MongoDB\\Driver\\Session::isInTransaction »'
  - index.md: PHP Manual
  - class.mongodb-driver-session.md: MongoDB\\Driver\\Session
title: 'MongoDB\\Driver\\Session::isDirty'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Session::isDirty

(mongodb >=1.13.0)

MongoDB\\Driver\\Session::isDirty - Повертає, чи була сесія позначена як брудна

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

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
