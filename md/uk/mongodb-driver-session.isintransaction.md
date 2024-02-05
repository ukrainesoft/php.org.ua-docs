---
navigation:
  - mongodb-driver-session.isdirty.md: '« MongoDB\\Driver\\Session::isDirty'
  - mongodb-driver-session.starttransaction.md: 'MongoDB\\Driver\\Session::startTransaction »'
  - index.md: PHP Manual
  - class.mongodb-driver-session.md: MongoDB\\Driver\\Session
title: 'MongoDB\\Driver\\Session::isInTransaction'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Session::isInTransaction

(mongodb >=1.6.0)

MongoDB\\Driver\\Session::isInTransaction — Визначає, чи відбувається багатодокументна транзакція.

### Опис

```methodsynopsis
final public MongoDB\Driver\Session::isInTransaction(): boolean
```

Визначає, чи відбувається зараз у поточній сесії багатодокументна транзакція. Вважається, що транзакція "відбувається прямо зараз", якщо вона була запущена, але поки не була підтверджена ні скасована.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**или**`false`**

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Session::getTransactionState()](mongodb-driver-session.gettransactionstate.md) \- Повертає статус транзакції для поточної сесії
