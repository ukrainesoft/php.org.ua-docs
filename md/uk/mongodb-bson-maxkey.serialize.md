---
navigation:
  - mongodb-bson-maxkey.jsonserialize.md: '« MongoDB\\BSON\\MaxKey::jsonSerialize'
  - mongodb-bson-maxkey.unserialize.md: 'MongoDB\\BSON\\MaxKey::unserialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-maxkey.md: MongoDB\\BSON\\MaxKey
title: 'MongoDB\\BSON\\MaxKey::serialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\MaxKey::serialize

(mongodb >=1.2.0)

MongoDB\\BSON\\MaxKey::serialize — Серіалізує MaxKey

### Опис

```methodsynopsis
final public MongoDB\BSON\MaxKey::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Возвращает сериализованное представление[MongoDB\\BSON\\MaxKey](class.mongodb-bson-maxkey.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\BSON\\MaxKey::unserialize()](mongodb-bson-maxkey.unserialize.md) \- Десеріалізує MaxKey
-   [serialize()](function.serialize.md) \- Генерує придатне для зберігання уявлення змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
