---
navigation:
  - mongodb-driver-session.getserver.md: '« MongoDB\\Driver\\Session::getServer'
  - mongodb-driver-session.gettransactionstate.md: 'MongoDB\\Driver\\Session::getTransactionState »'
  - index.md: PHP Manual
  - class.mongodb-driver-session.md: MongoDB\\Driver\\Session
title: 'MongoDB\\Driver\\Session::getTransactionOptions'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Session::getTransactionOptions

(mongodb >=1.7.0)

MongoDB\\Driver\\Session::getTransactionOptions — Повертає установки поточної транзакції

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

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Session::getTransactionState()](mongodb-driver-session.gettransactionstate.md) \- Повертає статус транзакції для поточної сесії
