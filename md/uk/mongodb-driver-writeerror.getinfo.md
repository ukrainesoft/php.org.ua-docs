---
navigation:
  - mongodb-driver-writeerror.getindex.md: '« MongoDB\\Driver\\WriteError::getIndex'
  - mongodb-driver-writeerror.getmessage.md: 'MongoDB\\Driver\\WriteError::getMessage »'
  - index.md: PHP Manual
  - class.mongodb-driver-writeerror.md: MongoDB\\Driver\\WriteError
title: 'MongoDB\\Driver\\WriteError::getInfo'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\WriteError::getInfo

(mongodb >=1.0.0)

MongoDB\\Driver\\WriteError::getInfo — Повертає документ метаданих для WriteError

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteError::getInfo(): ?object
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає документ метаданих для WriteError, або **`null`**, якщо метадані недоступні.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
