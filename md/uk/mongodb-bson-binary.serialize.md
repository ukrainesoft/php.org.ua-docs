---
navigation:
  - mongodb-bson-binary.jsonserialize.md: '« MongoDB\\BSON\\Binary::jsonSerialize'
  - mongodb-bson-binary.tostring.md: 'MongoDB\\BSON\\Binary::\_\_toString »'
  - index.md: PHP Manual
  - class.mongodb-bson-binary.md: MongoDB\\BSON\\Binary
title: 'MongoDB\\BSON\\Binary::serialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Binary::serialize

(mongodb >=1.2.0)

MongoDB\\BSON\\Binary::serialize — Серіалізує Binary

### Опис

```methodsynopsis
final public MongoDB\BSON\Binary::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Возвращает сериализованное представление[MongoDB\\BSON\\Binary](class.mongodb-bson-binary.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\BSON\\Binary::unserialize()](mongodb-bson-binary.unserialize.md) \- Десеріалізує Binary
-   [serialize()](function.serialize.md) \- Генерує придатне для зберігання уявлення змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
