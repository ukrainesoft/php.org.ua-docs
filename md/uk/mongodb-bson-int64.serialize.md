---
navigation:
  - mongodb-bson-int64.jsonserialize.md: '« MongoDBBSONInt64::jsonSerialize'
  - mongodb-bson-int64.tostring.md: 'MongoDBBSONInt64::toString »'
  - index.md: PHP Manual
  - class.mongodb-bson-int64.md: MongoDBBSONInt64
title: 'MongoDBBSONInt64::serialize'
---
# MongoDBBSONInt64::serialize

(mongodb >=1.5.0)

MongoDBBSONInt64::serialize — Серіалізує Int64

### Опис

```methodsynopsis
final public MongoDB\BSON\Int64::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDBBSONInt64](class.mongodb-bson-int64.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBBSONInt64::unserialize()](mongodb-bson-int64.unserialize.md) - Десеріалізує Int64
-   [serialize()](function.serialize.md) - Генерує придатне для зберігання подання змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
