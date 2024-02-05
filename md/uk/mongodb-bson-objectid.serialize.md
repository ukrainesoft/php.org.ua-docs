---
navigation:
  - mongodb-bson-objectid.jsonserialize.md: '« MongoDB\\BSON\\ObjectId::jsonSerialize'
  - mongodb-bson-objectid.tostring.md: 'MongoDB\\BSON\\ObjectId::\_\_toString »'
  - index.md: PHP Manual
  - class.mongodb-bson-objectid.md: MongoDB\\BSON\\ObjectId
title: 'MongoDB\\BSON\\ObjectId::serialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\ObjectId::serialize

(mongodb >=1.2.0)

MongoDB\\BSON\\ObjectId::serialize — Серіалізує ObjectId

### Опис

```methodsynopsis
final public MongoDB\BSON\ObjectId::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Возвращает сериализованное представление[MongoDB\\BSON\\ObjectId](class.mongodb-bson-objectid.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\BSON\\ObjectId::unserialize()](mongodb-bson-objectid.unserialize.md) \- Десеріалізує ObjectId
-   [serialize()](function.serialize.md) \- Генерує придатне для зберігання уявлення змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
