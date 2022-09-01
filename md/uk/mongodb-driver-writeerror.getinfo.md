---
navigation:
  - mongodb-driver-writeerror.getindex.html: '« MongoDBDriverWriteError::getIndex'
  - mongodb-driver-writeerror.getmessage.html: 'MongoDBDriverWriteError::getMessage »'
  - index.md: PHP Manual
  - class.mongodb-driver-writeerror.html: MongoDBDriverWriteError
title: 'MongoDBDriverWriteError::getInfo'
---
# MongoDBDriverWriteError::getInfo

(mongodb >=1.0.0)

MongoDBDriverWriteError::getInfo — Повертає документ метаданих для WriteError

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteError::getInfo(): ?object
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає документ метаданих для WriteError, або **`null`**, якщо метадані недоступні.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
