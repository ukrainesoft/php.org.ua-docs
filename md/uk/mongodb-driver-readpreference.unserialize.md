---
navigation:
  - mongodb-driver-readpreference.serialize.md: '« MongoDB\\Driver\\ReadPreference::serialize'
  - class.mongodb-driver-readconcern.md: MongoDB\\Driver\\ReadConcern »
  - index.md: PHP Manual
  - class.mongodb-driver-readpreference.md: MongoDB\\Driver\\ReadPreference
title: 'MongoDB\\Driver\\ReadPreference::unserialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ReadPreference::unserialize

(mongodb >=1.7.0)

MongoDB\\Driver\\ReadPreference::unserialize — Десеріалізація ReadPreference

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadPreference::unserialize(string $data): void
```

### Список параметрів

`data`

Серіалізований [MongoDB\\Driver\\ReadPreference](class.mongodb-driver-readpreference.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Кидає виняток [MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md)якщо виникла неможливо зробити десеріалізацію властивості, наприклад, якщо значення`serialized`не коректно.
-   Кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо властивості не коректні, наприклад, пропущені поля або вони мають некоректні значення.

### Дивіться також

-   [MongoDB\\Driver\\ReadPreference::serialize()](mongodb-driver-readpreference.serialize.md) \- Серіалізація ReadPreference
-   [unserialize()](function.unserialize.md) \- Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
