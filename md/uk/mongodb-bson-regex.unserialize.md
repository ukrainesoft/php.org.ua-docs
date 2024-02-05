---
navigation:
  - mongodb-bson-regex.tostring.md: '« MongoDB\\BSON\\Regex::\_\_function toString() { [native code] }'
  - class.mongodb-bson-timestamp.md: MongoDB\\BSON\\Timestamp »
  - index.md: PHP Manual
  - class.mongodb-bson-regex.md: MongoDB\\BSON\\Regex
title: 'MongoDB\\BSON\\Regex::unserialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Regex::unserialize

(mongodb >=1.2.0)

MongoDB\\BSON\\Regex::unserialize — Десеріалізує Regex

### Опис

```methodsynopsis
final public MongoDB\BSON\Regex::unserialize(string $data): void
```

### Список параметрів

`data`

Серіалізований [MongoDB\\BSON\\Regex](class.mongodb-bson-regex.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Видає[MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md)якщо властивості не можуть бути не серіалізовані (наприклад,`serialized`був неправильно сформований).
-   Видає[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо властивості неприпустимі (наприклад, відсутні поля або неприпустимі значення).

### Дивіться також

-   [MongoDB\\BSON\\Regex::serialize()](mongodb-bson-regex.serialize.md) \- Серіалізує Regex
-   [unserialize()](function.unserialize.md) \- Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
