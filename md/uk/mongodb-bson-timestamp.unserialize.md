---
navigation:
  - mongodb-bson-timestamp.tostring.md: '« MongoDB\\BSON\\Timestamp::\_\_function toString() { [native code] }'
  - class.mongodb-bson-utcdatetime.md: MongoDB\\BSON\\UTCDateTime »
  - index.md: PHP Manual
  - class.mongodb-bson-timestamp.md: MongoDB\\BSON\\Timestamp
title: 'MongoDB\\BSON\\Timestamp::unserialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Timestamp::unserialize

(mongodb >=1.2.0)

MongoDB\\BSON\\Timestamp::unserialize — Десеріалізує Timestamp

### Опис

```methodsynopsis
final public MongoDB\BSON\Timestamp::unserialize(string $data): void
```

### Список параметрів

`data`

Серіалізований [MongoDB\\BSON\\Timestamp](class.mongodb-bson-timestamp.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Видає[MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md)якщо властивості не можуть бути не серіалізовані (наприклад,`serialized`був неправильно сформований).
-   Видає[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо властивості неприпустимі (наприклад, відсутні поля або неприпустимі значення).

### Дивіться також

-   [MongoDB\\BSON\\Timestamp::serialize()](mongodb-bson-timestamp.serialize.md) \- Серіалізує Timestamp
-   [unserialize()](function.unserialize.md) \- Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
