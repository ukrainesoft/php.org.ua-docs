---
navigation:
  - mongodb-driver-cursorinterface.getid.md: '« MongoDBDriverCursorInterface::getId'
  - mongodb-driver-cursorinterface.isdead.md: 'MongoDBDriverCursorInterface::isDead »'
  - index.md: PHP Manual
  - class.mongodb-driver-cursorinterface.md: MongoDBDriverCursorInterface
title: 'MongoDBDriverCursorInterface::getServer'
---
# MongoDBDriverCursorInterface::getServer

(mongodb >=1.6.0)

MongoDBDriverCursorInterface::getServer — Повертає сервер, з яким пов'язаний курсор

### Опис

```methodsynopsis
abstract public MongoDB\Driver\CursorInterface::getServer(): MongoDB\Driver\Server
```

Повертає [MongoDBDriverServer](class.mongodb-driver-server.md) пов'язаний із курсором. Це той сервер, на якому запущено [MongoDBDriverQuery](class.mongodb-driver-query.md) або [MongoDBDriverCommand](class.mongodb-driver-command.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDBDriverServer](class.mongodb-driver-server.md) пов'язаний із курсором.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverCursor::getServer()](mongodb-driver-cursor.getserver.md) - Повертає сервер, пов'язаний із курсором
-   [MongoDBDriverServer](class.mongodb-driver-server.md)
