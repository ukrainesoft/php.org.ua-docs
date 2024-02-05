---
navigation:
  - mongodb-bson-dbpointer.jsonserialize.md: '« MongoDB\\BSON\\DBPointer::jsonSerialize'
  - mongodb-bson-dbpointer.tostring.md: 'MongoDB\\BSON\\DBPointer::\_\_toString »'
  - index.md: PHP Manual
  - class.mongodb-bson-dbpointer.md: MongoDB\\BSON\\DBPointer
title: 'MongoDB\\BSON\\DBPointer::serialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\DBPointer::serialize

(mongodb >=1.4.0)

MongoDB\\BSON\\DBPointer::serialize — Серіалізує DBPointer

### Опис

```methodsynopsis
final public MongoDB\BSON\DBPointer::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Возвращает сериализованное представление[MongoDB\\BSON\\DBPointer](class.mongodb-bson-dbpointer.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\BSON\\DBPointer::unserialize()](mongodb-bson-dbpointer.unserialize.md) \- Десеріалізує DBPointer
-   [serialize()](function.serialize.md) \- Генерує придатне для зберігання уявлення змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
