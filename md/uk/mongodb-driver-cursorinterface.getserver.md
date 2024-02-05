---
navigation:
  - mongodb-driver-cursorinterface.getid.md: '« MongoDB\\Driver\\CursorInterface::getId'
  - mongodb-driver-cursorinterface.isdead.md: 'MongoDB\\Driver\\CursorInterface::isDead »'
  - index.md: PHP Manual
  - class.mongodb-driver-cursorinterface.md: MongoDB\\Driver\\CursorInterface
title: 'MongoDB\\Driver\\CursorInterface::getServer'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\CursorInterface::getServer

(mongodb >=1.6.0)

MongoDB\\Driver\\CursorInterface::getServer — Повертає сервер, з яким пов'язаний курсор

### Опис

```methodsynopsis
abstract public MongoDB\Driver\CursorInterface::getServer(): MongoDB\Driver\Server
```

Повертає [MongoDB\\Driver\\Server](class.mongodb-driver-server.md) пов'язаний із курсором. Це той сервер, на якому запущено [MongoDB\\Driver\\Query](class.mongodb-driver-query.md) або [MongoDB\\Driver\\Command](class.mongodb-driver-command.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDB\\Driver\\Server](class.mongodb-driver-server.md) пов'язаний із курсором.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Cursor::getServer()](mongodb-driver-cursor.getserver.md) \- Повертає сервер, пов'язаний із курсором
-   [MongoDB\\Driver\\Server](class.mongodb-driver-server.md)
