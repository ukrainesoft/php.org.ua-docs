---
navigation:
  - class.mongodb-driver-exception-commandexception.md: « MongoDB\\Driver\\Exception\\CommandException
  - class.mongodb-driver-exception-connectionexception.md: MongoDB\\Driver\\Exception\\ConnectionException »
  - index.md: PHP Manual
  - class.mongodb-driver-exception-commandexception.md: MongoDB\\Driver\\Exception\\CommandException
title: 'MongoDB\\Driver\\Exception\\CommandException::getResultDocument'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Exception\\CommandException::getResultDocument

(mongodb >= 1.5.0)

MongoDB\\Driver\\Exception\\CommandException::getResultDocument — Повертає результат документа для невдалої команди

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

-   [MongoDB\\Driver\\Manager::executeCommand()](mongodb-driver-manager.executecommand.md) \- Виконує команду бази даних
