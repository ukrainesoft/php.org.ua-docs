---
navigation:
  - mongodb-bson-decimal128.jsonserialize.md: '« MongoDB\\BSON\\Decimal128::jsonSerialize'
  - mongodb-bson-decimal128.tostring.md: 'MongoDB\\BSON\\Decimal128::\_\_toString »'
  - index.md: PHP Manual
  - class.mongodb-bson-decimal128.md: MongoDB\\BSON\\Decimal128
title: 'MongoDB\\BSON\\Decimal128::serialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Decimal128::serialize

(mongodb >=1.2.0)

MongoDB\\BSON\\Decimal128::serialize — Серіалізує Decimal128

### Опис

```methodsynopsis
final public MongoDB\BSON\Decimal128::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Возвращает сериализованное представление[MongoDB\\BSON\\Decimal128](class.mongodb-bson-decimal128.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\BSON\\Decimal128::unserialize()](mongodb-bson-decimal128.unserialize.md) \- Десеріалізує Decimal128
-   [serialize()](function.serialize.md) \- Генерує придатне для зберігання уявлення змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
