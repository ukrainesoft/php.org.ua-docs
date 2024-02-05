---
navigation:
  - mongodb-bson-utcdatetime.jsonserialize.md: '« MongoDB\\BSON\\UTCDateTime::jsonSerialize'
  - mongodb-bson-utcdatetime.todatetime.md: 'MongoDB\\BSON\\UTCDateTime::toDateTime »'
  - index.md: PHP Manual
  - class.mongodb-bson-utcdatetime.md: MongoDB\\BSON\\UTCDateTime
title: 'MongoDB\\BSON\\UTCDateTime::serialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\UTCDateTime::serialize

(mongodb >=1.2.0)

MongoDB\\BSON\\UTCDateTime::serialize — Серіалізує UTCDateTime

### Опис

```methodsynopsis
final public MongoDB\BSON\UTCDateTime::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Возвращает сериализованное представление[MongoDB\\BSON\\UTCDateTime](class.mongodb-bson-utcdatetime.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\BSON\\UTCDateTime::unserialize()](mongodb-bson-utcdatetime.unserialize.md) \- Десеріалізує UTCDateTime
-   [serialize()](function.serialize.md) \- Генерує придатне для зберігання уявлення змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
