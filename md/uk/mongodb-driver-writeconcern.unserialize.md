---
navigation:
  - mongodb-driver-writeconcern.serialize.md: '« MongoDB\\Driver\\WriteConcern::serialize'
  - class.mongodb-driver-readpreference.md: MongoDB\\Driver\\ReadPreference »
  - index.md: PHP Manual
  - class.mongodb-driver-writeconcern.md: MongoDB\\Driver\\WriteConcern
title: 'MongoDB\\Driver\\WriteConcern::unserialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\WriteConcern::unserialize

(mongodb >=1.7.0)

MongoDB\\Driver\\WriteConcern::unserialize — Десеріалізація WriteConcern

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteConcern::unserialize(string $data): void
```

### Список параметрів

`data`

Серіалізований [MongoDB\\Driver\\WriteConcern](class.mongodb-driver-writeconcern.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Кидає виняток [MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md)якщо виникла неможливо зробити десеріалізацію властивості, наприклад, якщо значення`serialized`не коректно.
-   Кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо властивості не коректні, наприклад, пропущені поля або вони мають некоректні значення.

### Дивіться також

-   [MongoDB\\Driver\\WriteConcern::serialize()](mongodb-driver-writeconcern.serialize.md) \- Серіалізація WriteConcern
-   [unserialize()](function.unserialize.md) \- Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
