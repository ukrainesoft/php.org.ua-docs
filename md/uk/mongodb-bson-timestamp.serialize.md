---
navigation:
  - mongodb-bson-timestamp.jsonserialize.html: '« MongoDBBSONTimestamp::jsonSerialize'
  - mongodb-bson-timestamp.tostring.html: 'MongoDBBSONTimestamp::toString »'
  - index.md: PHP Manual
  - class.mongodb-bson-timestamp.html: MongoDBBSONTimestamp
title: 'MongoDBBSONTimestamp::serialize'
---
# MongoDBBSONTimestamp::serialize

(mongodb >=1.2.0)

MongoDBBSONTimestamp::serialize — Серіалізує Timestamp

### Опис

```methodsynopsis
final public MongoDB\BSON\Timestamp::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDBBSONTimestamp](class.mongodb-bson-timestamp.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBBSONTimestamp::unserialize()](mongodb-bson-timestamp.unserialize.html) - Десеріалізує Timestamp
-   [serialize()](function.serialize.md) - Генерує придатне для зберігання уявлення змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
