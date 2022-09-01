---
navigation:
  - mongodb-bson-binary.jsonserialize.html: '« MongoDBBSONBinary::jsonSerialize'
  - mongodb-bson-binary.tostring.html: 'MongoDBBSONBinary::toString »'
  - index.html: PHP Manual
  - class.mongodb-bson-binary.html: MongoDBBSONBinary
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

Повертає серіалізовану виставу [MongoDBBSONBinary](class.mongodb-bson-binary.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBBSONBinary::unserialize()](mongodb-bson-binary.unserialize.html) - Десеріалізує Binary
-   [serialize()](function.serialize.html) - Генерує придатне для зберігання уявлення змінної
-   [Серіалізація об'єктів](language.oop5.serialization.html)
