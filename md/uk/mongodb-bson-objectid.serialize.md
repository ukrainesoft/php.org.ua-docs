---
navigation:
  - mongodb-bson-objectid.jsonserialize.html: '« MongoDBBSONObjectId::jsonSerialize'
  - mongodb-bson-objectid.tostring.html: 'MongoDBBSONObjectId::toString »'
  - index.md: PHP Manual
  - class.mongodb-bson-objectid.html: MongoDBBSONObjectId
title: 'MongoDBBSONObjectId::serialize'
---
# MongoDBBSONObjectId::serialize

(mongodb >=1.2.0)

MongoDBBSONObjectId::serialize — Серіалізує ObjectId

### Опис

```methodsynopsis
final public MongoDB\BSON\ObjectId::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDBBSONObjectId](class.mongodb-bson-objectid.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBBSONObjectId::unserialize()](mongodb-bson-objectid.unserialize.md) - Десеріалізує ObjectId
-   [serialize()](function.serialize.md) - Генерує придатне для зберігання подання змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
