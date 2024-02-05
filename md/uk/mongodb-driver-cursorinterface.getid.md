---
navigation:
  - class.mongodb-driver-cursorinterface.md: « MongoDB\\Driver\\CursorInterface
  - mongodb-driver-cursorinterface.getserver.md: 'MongoDB\\Driver\\CursorInterface::getServer »'
  - index.md: PHP Manual
  - class.mongodb-driver-cursorinterface.md: MongoDB\\Driver\\CursorInterface
title: 'MongoDB\\Driver\\CursorInterface::getId'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\CursorInterface::getId

(mongodb >=1.6.0)

MongoDB\\Driver\\CursorInterface::getId — Повертає ідентифікатор курсору

### Опис

```methodsynopsis
abstract public MongoDB\Driver\CursorInterface::getId(): MongoDB\Driver\CursorId
```

Повертає [MongoDB\\Driver\\CursorId](class.mongodb-driver-cursorid.md) пов'язаний із курсором. Кожен курсор має унікальний ідентифікатор.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDB\\Driver\\CursorId](class.mongodb-driver-cursorid.md)для курсора.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Cursor::getId()](mongodb-driver-cursor.getid.md) \- Повертає ідентифікатор для курсору
-   [MongoDB\\Driver\\CursorId](class.mongodb-driver-cursorid.md)
-   [MongoDB\\Driver\\CursorId::\_\_toString()](mongodb-driver-cursorid.tostring.md) \- Строкове подання ідентифікатора курсору
