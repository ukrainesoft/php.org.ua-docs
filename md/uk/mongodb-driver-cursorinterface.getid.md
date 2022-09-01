---
navigation:
  - class.mongodb-driver-cursorinterface.html: « MongoDBDriverCursorInterface
  - mongodb-driver-cursorinterface.getserver.html: 'MongoDBDriverCursorInterface::getServer »'
  - index.html: PHP Manual
  - class.mongodb-driver-cursorinterface.html: MongoDBDriverCursorInterface
title: 'MongoDBDriverCursorInterface::getId'
---
# MongoDBDriverCursorInterface::getId

(mongodb >=1.6.0)

MongoDBDriverCursorInterface::getId — Повертає ідентифікатор курсору

### Опис

```methodsynopsis
abstract public MongoDB\Driver\CursorInterface::getId(): MongoDB\Driver\CursorId
```

Повертає [MongoDBDriverCursorId](class.mongodb-driver-cursorid.html) пов'язаний із курсором. Кожен курсор має унікальний ідентифікатор.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDBDriverCursorId](class.mongodb-driver-cursorid.html) для курсору.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverCursor::getId()](mongodb-driver-cursor.getid.html) - Повертає ідентифікатор для курсору
-   [MongoDBDriverCursorId](class.mongodb-driver-cursorid.html)
-   [MongoDBDriverCursorId::toString()](mongodb-driver-cursorid.tostring.html) - Строкове подання ідентифікатора курсору
