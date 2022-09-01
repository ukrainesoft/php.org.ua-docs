---
navigation:
  - mongodb-bson-utcdatetime.jsonserialize.html: '« MongoDBBSONUTCDateTime::jsonSerialize'
  - mongodb-bson-utcdatetime.todatetime.html: 'MongoDBBSONUTCDateTime::toDateTime »'
  - index.html: PHP Manual
  - class.mongodb-bson-utcdatetime.html: MongoDBBSONUTCDateTime
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

Повертає серіалізовану виставу [MongoDBBSONUTCDateTime](class.mongodb-bson-utcdatetime.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBBSONUTCDateTime::unserialize()](mongodb-bson-utcdatetime.unserialize.html) - Десеріалізує UTCDateTime
-   [serialize()](function.serialize.html) - Генерує придатне для зберігання подання змінної
-   [Серіалізація об'єктів](language.oop5.serialization.html)
