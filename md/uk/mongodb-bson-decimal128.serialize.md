---
navigation:
  - mongodb-bson-decimal128.jsonserialize.html: '« MongoDBBSONDecimal128::jsonSerialize'
  - mongodb-bson-decimal128.tostring.html: 'MongoDBBSONDecimal128::toString »'
  - index.html: PHP Manual
  - class.mongodb-bson-decimal128.html: MongoDBBSONDecimal128
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

Повертає серіалізовану виставу [MongoDBBSONDecimal128](class.mongodb-bson-decimal128.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBBSONDecimal128::unserialize()](mongodb-bson-decimal128.unserialize.html) - Десеріалізує Decimal128
-   [serialize()](function.serialize.html) - Генерує придатне для зберігання подання змінної
-   [Серіалізація об'єктів](language.oop5.serialization.html)
