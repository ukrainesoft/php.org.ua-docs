---
navigation:
  - class.mongodb-driver-exception-commandexception.html: « MongoDBDriverExceptionCommandException
  - class.mongodb-driver-exception-connectionexception.html: MongoDBDriverExceptionConnectionException »
  - index.md: PHP Manual
  - class.mongodb-driver-exception-commandexception.html: MongoDBDriverExceptionCommandException
title: 'MongoDBDriverExceptionCommandException::getResultDocument'
---
# MongoDBDriverExceptionCommandException::getResultDocument

(mongodb >= 1.5.0)

MongoDBDriverExceptionCommandException::getResultDocument — Повертає результат документа для невдалої команди

### Опис

```methodsynopsis
final public MongoDB\Driver\Exception\CommandException::getResultDocument(): object
```

Повертає результат документа для невдалої команди.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Документ результату для невдалої команди.

### Дивіться також

-   [MongoDBDriverManager::executeCommand()](mongodb-driver-manager.executecommand.html) - Виконує команду бази даних
