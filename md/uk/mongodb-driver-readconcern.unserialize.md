---
navigation:
  - mongodb-driver-readconcern.serialize.md: '« MongoDB\\Driver\\ReadConcern::serialize'
  - class.mongodb-driver-cursor.md: MongoDB\\Driver\\Cursor »
  - index.md: PHP Manual
  - class.mongodb-driver-readconcern.md: MongoDB\\Driver\\ReadConcern
title: 'MongoDB\\Driver\\ReadConcern::unserialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ReadConcern::unserialize

(mongodb >=1.7.0)

MongoDB\\Driver\\ReadConcern::unserialize — Десеріалізація ReadConcern

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadConcern::unserialize(string $data): void
```

### Список параметрів

`data`

Серіалізований [MongoDB\\Driver\\ReadConcern](class.mongodb-driver-readconcern.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Кидає виняток [MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md)якщо виникла неможливо зробити десеріалізацію властивості, наприклад, якщо значення`serialized`не коректно.
-   Кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо властивості не коректні, наприклад, пропущені поля або вони мають некоректні значення.

### Дивіться також

-   [MongoDB\\Driver\\ReadConcern::serialize()](mongodb-driver-readconcern.serialize.md) \- Серіалізація ReadConcern
-   [unserialize()](function.unserialize.md) \- Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
