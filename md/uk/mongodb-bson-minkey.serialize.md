---
navigation:
  - mongodb-bson-minkey.jsonserialize.md: '« MongoDB\\BSON\\MinKey::jsonSerialize'
  - mongodb-bson-minkey.unserialize.md: 'MongoDB\\BSON\\MinKey::unserialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-minkey.md: MongoDB\\BSON\\MinKey
title: 'MongoDB\\BSON\\MinKey::serialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\MinKey::serialize

(mongodb >=1.2.0)

MongoDB\\BSON\\MonKey::serialize — Серіалізує MonKey

### Опис

```methodsynopsis
final public MongoDB\BSON\MinKey::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Возвращает сериализованное представление[MongoDB\\BSON\\MinKey](class.mongodb-bson-minkey.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\BSON\\MinKey::unserialize()](mongodb-bson-minkey.unserialize.md) \- Десеріалізує MinKey
-   [serialize()](function.serialize.md) \- Генерує придатне для зберігання уявлення змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
