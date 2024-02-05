---
navigation:
  - mongodb-driver-serverapi.serialize.md: '« MongoDB\\Driver\\ServerApi::serialize'
  - class.mongodb-driver-writeconcern.md: MongoDB\\Driver\\WriteConcern »
  - index.md: PHP Manual
  - class.mongodb-driver-serverapi.md: MongoDB\\Driver\\ServerApi
title: 'MongoDB\\Driver\\ServerApi::unserialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ServerApi::unserialize

(mongodb >=1.10.0)

MongoDB\\Driver\\ServerApi::unserialize — Десеріалізує ServerApi

### Опис

```methodsynopsis
final public MongoDB\Driver\ServerApi::unserialize(string $data): void
```

### Список параметрів

`data`

Серіалізований [MongoDB\\Driver\\ServerApi](class.mongodb-driver-serverapi.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Викидає [MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md)якщо властивості не можуть бути десеріалізовані (наприклад,`serialized`було некоректно сформовано).
-   Викидає [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо властивості некоректні (наприклад, відсутні поля або містяться неприпустимі значення).

### Дивіться також

-   [MongoDB\\Driver\\ServerApi::serialize()](mongodb-driver-serverapi.serialize.md) \- Серіалізує ServerApi
-   [unserialize()](function.unserialize.md) \- Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
