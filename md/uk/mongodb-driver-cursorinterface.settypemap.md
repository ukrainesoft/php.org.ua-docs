---
navigation:
  - mongodb-driver-cursorinterface.isdead.md: '« MongoDB\\Driver\\CursorInterface::isDead'
  - mongodb-driver-cursorinterface.toarray.md: 'MongoDB\\Driver\\CursorInterface::toArray »'
  - index.md: PHP Manual
  - class.mongodb-driver-cursorinterface.md: MongoDB\\Driver\\CursorInterface
title: 'MongoDB\\Driver\\CursorInterface::setTypeMap'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\CursorInterface::setTypeMap

(mongodb >=1.6.0)

MongoDB\\Driver\\CursorInterface::setTypeMap — Задати порівняння типів для десеріалізації BSON

### Опис

```methodsynopsis
abstract public MongoDB\Driver\CursorInterface::setTypeMap(array $typemap): void
```

Задати [зіставлення типів](mongodb.persistence.deserialization.md#mongodb.persistence.typemaps)для использования при десериализации результатов BSON в значения PHP.

### Список параметрів

`typeMap`(array)

[Конфігурація карти типів](mongodb.persistence.deserialization.md#mongodb.persistence.typemaps)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Cursor::setTypeMap()](mongodb-driver-cursor.settypemap.md) \- Встановлює карту типу для десеріалізації BSON
-   [Постійні дані](mongodb.persistence.md)
