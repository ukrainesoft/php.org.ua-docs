---
navigation:
  - mongodb-driver-writeconcern.serialize.html: '« MongoDBDriverWriteConcern::serialize'
  - class.mongodb-driver-readpreference.html: MongoDBDriverReadPreference »
  - index.md: PHP Manual
  - class.mongodb-driver-writeconcern.html: MongoDBDriverWriteConcern
title: 'MongoDBDriverWriteConcern::unserialize'
---
# MongoDBDriverWriteConcern::unserialize

(mongodb >=1.7.0)

MongoDBDriverWriteConcern::unserialize — Десеріалізація WriteConcern

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteConcern::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDBDriverWriteConcern](class.mongodb-driver-writeconcern.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Кидає виняток [MongoDBDriverExceptionUnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md) якщо виникла неможливо зробити десеріалізацію властивості, наприклад, якщо значення `serialized` не коректно.
-   Кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md) якщо властивості не коректні, наприклад, пропущені поля або вони мають некоректні значення.

### Дивіться також

-   [MongoDBDriverWriteConcern::serialize()](mongodb-driver-writeconcern.serialize.md) - Серіалізація WriteConcern
-   [unserialize()](function.unserialize.md) - Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
