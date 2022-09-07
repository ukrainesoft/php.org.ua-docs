---
navigation:
  - mongodb-bson-decimal128.jsonserialize.md: '« MongoDBBSONDecimal128::jsonSerialize'
  - mongodb-bson-decimal128.tostring.md: 'MongoDBBSONDecimal128::toString »'
  - index.md: PHP Manual
  - class.mongodb-bson-decimal128.md: MongoDBBSONDecimal128
title: 'MongoDBBSONDecimal128::serialize'
---
# MongoDBBSONDecimal128::serialize

(mongodb >=1.2.0)

MongoDBBSONDecimal128::serialize — Серіалізує Decimal128

### Опис

```methodsynopsis
final public MongoDB\BSON\Decimal128::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDBBSONDecimal128](class.mongodb-bson-decimal128.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBBSONDecimal128::unserialize()](mongodb-bson-decimal128.unserialize.md) - Десеріалізує Decimal128
-   [serialize()](function.serialize.md) - Генерує придатне для зберігання подання змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
