---
navigation:
  - mongodb-driver-readconcern.serialize.html: '« MongoDBDriverReadConcern::serialize'
  - class.mongodb-driver-cursor.html: MongoDBDriverCursor »
  - index.md: PHP Manual
  - class.mongodb-driver-readconcern.html: MongoDBDriverReadConcern
title: 'MongoDBDriverReadConcern::unserialize'
---
# MongoDBDriverReadConcern::unserialize

(mongodb >=1.7.0)

MongoDBDriverReadConcern::unserialize — Десеріалізація ReadConcern

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadConcern::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDBDriverReadConcern](class.mongodb-driver-readconcern.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Кидає виняток [MongoDBDriverExceptionUnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md) якщо виникла неможливо зробити десеріалізацію властивості, наприклад, якщо значення `serialized` не коректно.
-   Кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md) якщо властивості не коректні, наприклад, пропущені поля або вони мають некоректні значення.

### Дивіться також

-   [MongoDBDriverReadConcern::serialize()](mongodb-driver-readconcern.serialize.md) - Серіалізація ReadConcern
-   [unserialize()](function.unserialize.md) - Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
