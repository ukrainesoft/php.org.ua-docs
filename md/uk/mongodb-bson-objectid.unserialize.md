---
navigation:
  - mongodb-bson-objectid.tostring.md: '« MongoDB\\BSON\\ObjectId::\_\_function toString() { [native code] }'
  - class.mongodb-bson-regex.md: MongoDB\\BSON\\Regex »
  - index.md: PHP Manual
  - class.mongodb-bson-objectid.md: MongoDB\\BSON\\ObjectId
title: 'MongoDB\\BSON\\ObjectId::unserialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\ObjectId::unserialize

(mongodb >=1.2.0)

MongoDB\\BSON\\ObjectId::unserialize — Десеріалізує ObjectId

### Опис

```methodsynopsis
final public MongoDB\BSON\ObjectId::unserialize(string $data): void
```

### Список параметрів

`data`

Серіалізований [MongoDB\\BSON\\ObjectId](class.mongodb-bson-objectid.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Видає виняток[MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md)якщо властивості не можуть бути десеріалізовані (наприклад,`serialized`був неправильно сформований).
-   Видає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо властивості недійсні (наприклад, відсутні поля або неприпустимі значення).

### Дивіться також

-   [MongoDB\\BSON\\ObjectId::serialize()](mongodb-bson-objectid.serialize.md) \- Серіалізує ObjectId
-   [unserialize()](function.unserialize.md) \- Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
