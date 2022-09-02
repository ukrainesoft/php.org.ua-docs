---
navigation:
  - mongodb-bson-binary.jsonserialize.md: '« MongoDBBSONBinary::jsonSerialize'
  - mongodb-bson-binary.tostring.md: 'MongoDBBSONBinary::toString »'
  - index.md: PHP Manual
  - class.mongodb-bson-binary.md: MongoDBBSONBinary
title: 'MongoDBBSONBinary::serialize'
---
# MongoDBBSONBinary::serialize

(mongodb >=1.2.0)

MongoDBBSONBinary::serialize — Серіалізує Binary

### Опис

```methodsynopsis
final public MongoDB\BSON\Binary::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDBBSONBinary](class.mongodb-bson-binary.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBBSONBinary::unserialize()](mongodb-bson-binary.unserialize.md) - Десеріалізує Binary
-   [serialize()](function.serialize.md) - Генерує придатне для зберігання уявлення змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
