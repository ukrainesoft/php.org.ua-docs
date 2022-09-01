---
navigation:
  - mongodb-driver-cursorinterface.settypemap.html: '« MongoDBDriverCursorInterface::setTypeMap'
  - class.mongodb-driver-server.html: MongoDBDriverServer »
  - index.md: PHP Manual
  - class.mongodb-driver-cursorinterface.html: MongoDBDriverCursorInterface
title: 'MongoDBDriverCursorInterface::toArray'
---
# MongoDBDriverCursorInterface::toArray

(mongodb >=1.6.0)

MongoDBDriverCursorInterface::toArray — Повернути всі результати для даного курсору у вигляді масиву

### Опис

```methodsynopsis
abstract public MongoDB\Driver\CursorInterface::toArray(): array
```

Ітерує курсор та повертає результати у вигляді масиву. Для контролю десеріалізації типи PHP можна використовувати [MongoDBDriverCursorInterface::setTypeMap()](mongodb-driver-cursorinterface.settypemap.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив, що містить усі результати курсору.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverCursor::toArray()](mongodb-driver-cursor.toarray.html) - Повертає масив, що містить усі результати курсору
-   [MongoDBDriverCursorInterface::setTypeMap()](mongodb-driver-cursorinterface.settypemap.html) - Задати порівняння типів для десеріалізації BSON
