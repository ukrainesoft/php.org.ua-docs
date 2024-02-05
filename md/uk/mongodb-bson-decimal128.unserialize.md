---
navigation:
  - mongodb-bson-decimal128.tostring.md: '« MongoDB\\BSON\\Decimal128::\_\_function toString() { [native code] }'
  - class.mongodb-bson-javascript.md: MongoDB\\BSON\\Javascript »
  - index.md: PHP Manual
  - class.mongodb-bson-decimal128.md: MongoDB\\BSON\\Decimal128
title: 'MongoDB\\BSON\\Decimal128::unserialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Decimal128::unserialize

(mongodb >=1.2.0)

MongoDB\\BSON\\Decimal128::unserialize — Десеріалізує Decimal128

### Опис

```methodsynopsis
final public MongoDB\BSON\Decimal128::unserialize(string $data): void
```

### Список параметрів

`data`

Серіалізований [MongoDB\\BSON\\Decimal128](class.mongodb-bson-decimal128.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Видає виняток[MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md)якщо властивості не можуть бути десеріалізовані (наприклад, параметр`serialized`був спотворений).
-   Видає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо властивості недійсні (наприклад, відсутні поля або неприпустимі значення).

### Дивіться також

-   [MongoDB\\BSON\\Decimal128::serialize()](mongodb-bson-decimal128.serialize.md) \- Серіалізує Decimal128
-   [unserialize()](function.unserialize.md) \- Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
