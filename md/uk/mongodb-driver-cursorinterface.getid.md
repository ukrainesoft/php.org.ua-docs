---
navigation:
  - class.mongodb-driver-cursorinterface.md: « MongoDBDriverCursorInterface
  - mongodb-driver-cursorinterface.getserver.md: 'MongoDBDriverCursorInterface::getServer »'
  - index.md: PHP Manual
  - class.mongodb-driver-cursorinterface.md: MongoDBDriverCursorInterface
title: 'MongoDBDriverCursorInterface::getId'
---
# MongoDBDriverCursorInterface::getId

(mongodb >=1.6.0)

MongoDBDriverCursorInterface::getId — Повертає ідентифікатор курсору

### Опис

```methodsynopsis
abstract public MongoDB\Driver\CursorInterface::getId(): MongoDB\Driver\CursorId
```

Повертає [MongoDBDriverCursorId](class.mongodb-driver-cursorid.md) пов'язаний із курсором. Кожен курсор має унікальний ідентифікатор.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDBDriverCursorId](class.mongodb-driver-cursorid.md) для курсору.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverCursor::getId()](mongodb-driver-cursor.getid.md) - Повертає ідентифікатор для курсору
-   [MongoDBDriverCursorId](class.mongodb-driver-cursorid.md)
-   [MongoDBDriverCursorId::toString()](mongodb-driver-cursorid.tostring.md) - Строкове подання ідентифікатора курсору
