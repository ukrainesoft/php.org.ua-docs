---
navigation:
  - mongodb-bson-utcdatetime.tostring.md: '« MongoDB\\BSON\\UTCDateTime::\_\_function toString() { [native code] }'
  - class.mongodb-bson-type.md: MongoDB\\BSON\\Type »
  - index.md: PHP Manual
  - class.mongodb-bson-utcdatetime.md: MongoDB\\BSON\\UTCDateTime
title: 'MongoDB\\BSON\\UTCDateTime::unserialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\UTCDateTime::unserialize

(mongodb >=1.2.0)

MongoDB\\BSON\\UTCDateTime::unserialize — Десеріалізує UTCDateTime

### Опис

```methodsynopsis
final public MongoDB\BSON\UTCDateTime::unserialize(string $data): void
```

### Список параметрів

`data`

Серіалізований [MongoDB\\BSON\\UTCDateTime](class.mongodb-bson-utcdatetime.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Видає[MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md)якщо властивості не можуть бути не серіалізовані (наприклад,`serialized`був неправильно сформований).
-   Видає[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо властивості неприпустимі (наприклад, відсутні поля або неприпустимі значення).

### Дивіться також

-   [MongoDB\\BSON\\UTCDateTime::serialize()](mongodb-bson-utcdatetime.serialize.md) \- Серіалізує UTCDateTime
-   [unserialize()](function.unserialize.md) \- Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
