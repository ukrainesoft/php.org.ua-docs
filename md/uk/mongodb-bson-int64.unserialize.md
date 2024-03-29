---
navigation:
  - mongodb-bson-int64.tostring.md: '« MongoDB\\BSON\\Int64::\_\_function toString() { [native code] }'
  - class.mongodb-bson-symbol.md: MongoDB\\BSON\\Symbol »
  - index.md: PHP Manual
  - class.mongodb-bson-int64.md: MongoDB\\BSON\\Int64
title: 'MongoDB\\BSON\\Int64::unserialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Int64::unserialize

(mongodb >=1.5.0)

MongoDB\\BSON\\Int64::unserialize — Десеріалізує Int64

### Опис

```methodsynopsis
final public MongoDB\BSON\Int64::unserialize(string $data): void
```

### Список параметрів

`data`

Серіалізований [MongoDB\\BSON\\Int64](class.mongodb-bson-int64.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Видає виняток[MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md)якщо властивості не можуть бути не серіалізовані (тобто`serialized`був неправильно сформований).
-   Видає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо властивості неприпустимі (наприклад, відсутні поля або неприпустимі значення).

### Дивіться також

-   [MongoDB\\BSON\\Int64::serialize()](mongodb-bson-int64.serialize.md) \- Серіалізує Int64
-   [unserialize()](function.unserialize.md) \- Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
