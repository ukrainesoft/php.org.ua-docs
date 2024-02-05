---
navigation:
  - mongodb-bson-symbol.jsonserialize.md: '« MongoDB\\BSON\\Symbol::jsonSerialize'
  - mongodb-bson-symbol.tostring.md: 'MongoDB\\BSON\\Symbol::\_\_toString »'
  - index.md: PHP Manual
  - class.mongodb-bson-symbol.md: MongoDB\\BSON\\Symbol
title: 'MongoDB\\BSON\\Symbol::serialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Symbol::serialize

(mongodb >=1.4.0)

MongoDB\\BSON\\Symbol::serialize — Серіалізує Symbol

### Опис

```methodsynopsis
final public MongoDB\BSON\Symbol::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Возвращает сериализованное представление[MongoDB\\BSON\\Symbol](class.mongodb-bson-symbol.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\BSON\\Symbol::unserialize()](mongodb-bson-symbol.unserialize.md) \- Десеріалізує Symbol
-   [serialize()](function.serialize.md) \- Генерує придатне для зберігання уявлення змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
