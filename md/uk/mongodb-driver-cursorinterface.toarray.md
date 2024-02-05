---
navigation:
  - mongodb-driver-cursorinterface.settypemap.md: '« MongoDB\\Driver\\CursorInterface::setTypeMap'
  - class.mongodb-driver-server.md: MongoDB\\Driver\\Server »
  - index.md: PHP Manual
  - class.mongodb-driver-cursorinterface.md: MongoDB\\Driver\\CursorInterface
title: 'MongoDB\\Driver\\CursorInterface::toArray'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\CursorInterface::toArray

(mongodb >=1.6.0)

MongoDB\\Driver\\CursorInterface::toArray — Повернути всі результати для даного курсору у вигляді масиву

### Опис

```methodsynopsis
abstract public MongoDB\Driver\CursorInterface::toArray(): array
```

Ітерує курсор та повертає результати у вигляді масиву. Для контролю десеріалізації типи PHP можна використовувати [MongoDB\\Driver\\CursorInterface::setTypeMap()](mongodb-driver-cursorinterface.settypemap.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив, що містить усі результати курсору.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Cursor::toArray()](mongodb-driver-cursor.toarray.md) \- Повертає масив, що містить усі результати курсору
-   [MongoDB\\Driver\\CursorInterface::setTypeMap()](mongodb-driver-cursorinterface.settypemap.md) \- Задати порівняння типів для десеріалізації BSON
