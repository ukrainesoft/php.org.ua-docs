---
navigation:
  - mongodb-bson-utcdatetime.jsonserialize.md: '« MongoDBBSONUTCDateTime::jsonSerialize'
  - mongodb-bson-utcdatetime.todatetime.md: 'MongoDBBSONUTCDateTime::toDateTime »'
  - index.md: PHP Manual
  - class.mongodb-bson-utcdatetime.md: MongoDBBSONUTCDateTime
title: 'MongoDBBSONUTCDateTime::serialize'
---
# MongoDBBSONUTCDateTime::serialize

(mongodb >=1.2.0)

MongoDBBSONUTCDateTime::serialize — Серіалізує UTCDateTime

### Опис

```methodsynopsis
final public MongoDB\BSON\UTCDateTime::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDBBSONUTCDateTime](class.mongodb-bson-utcdatetime.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBBSONUTCDateTime::unserialize()](mongodb-bson-utcdatetime.unserialize.md) - Десеріалізує UTCDateTime
-   [serialize()](function.serialize.md) - Генерує придатне для зберігання подання змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
