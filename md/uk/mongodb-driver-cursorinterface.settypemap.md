---
navigation:
  - mongodb-driver-cursorinterface.isdead.html: '« MongoDBDriverCursorInterface::isDead'
  - mongodb-driver-cursorinterface.toarray.html: 'MongoDBDriverCursorInterface::toArray »'
  - index.md: PHP Manual
  - class.mongodb-driver-cursorinterface.html: MongoDBDriverCursorInterface
title: 'MongoDBDriverCursorInterface::setTypeMap'
---
# MongoDBDriverCursorInterface::setTypeMap

(mongodb >=1.6.0)

MongoDBDriverCursorInterface::setTypeMap — Задати порівняння типів для десеріалізації BSON

### Опис

```methodsynopsis
abstract public MongoDB\Driver\CursorInterface::setTypeMap(array $typemap): void
```

Задати [сопоставление типов](mongodb.persistence.deserialization.html#mongodb.persistence.typemaps) для використання при десеріалізації результатів BSON значення PHP.

### Список параметрів

`typeMap` (array)

[Конфігурація карти типів](mongodb.persistence.deserialization.html#mongodb.persistence.typemaps)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverCursor::setTypeMap()](mongodb-driver-cursor.settypemap.md) - Встановлює карту типу для десеріалізації BSON
-   [Постійні дані](mongodb.persistence.md)
