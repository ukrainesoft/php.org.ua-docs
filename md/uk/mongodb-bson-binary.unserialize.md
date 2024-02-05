---
navigation:
  - mongodb-bson-binary.tostring.md: '« MongoDB\\BSON\\Binary::\_\_function toString() { [native code] }'
  - class.mongodb-bson-decimal128.md: MongoDB\\BSON\\Decimal128 »
  - index.md: PHP Manual
  - class.mongodb-bson-binary.md: MongoDB\\BSON\\Binary
title: 'MongoDB\\BSON\\Binary::unserialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Binary::unserialize

(mongodb >=1.2.0)

MongoDB\\BSON\\Binary::unserialize — Десеріалізує Binary

### Опис

```methodsynopsis
final public MongoDB\BSON\Binary::unserialize(string $data): void
```

### Список параметрів

`data`

Серіалізований [MongoDB\\BSON\\Binary](class.mongodb-bson-binary.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Видає[MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md)якщо властивості не можуть бути десеріалізовані (наприклад,`serialized`був неправильно сформований).
-   Видає[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо властивості неприпустимі (наприклад, відсутні поля або неприпустимі значення).

### Дивіться також

-   [MongoDB\\BSON\\Binary::serialize()](mongodb-bson-binary.serialize.md) \- Серіалізує Binary
-   [unserialize()](function.unserialize.md) \- Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
