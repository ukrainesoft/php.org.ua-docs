---
navigation:
  - mongodb-driver-readpreference.serialize.html: '« MongoDBDriverReadPreference::serialize'
  - class.mongodb-driver-readconcern.html: MongoDBDriverReadConcern »
  - index.md: PHP Manual
  - class.mongodb-driver-readpreference.html: MongoDBDriverReadPreference
title: 'MongoDBDriverReadPreference::unserialize'
---
# MongoDBDriverReadPreference::unserialize

(mongodb >=1.7.0)

MongoDBDriverReadPreference::unserialize — Десеріалізація ReadPreference

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadPreference::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDBDriverReadPreference](class.mongodb-driver-readpreference.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Кидає виняток [MongoDBDriverExceptionUnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html)якщо виникла неможливо зробити десеріалізацію властивості, наприклад, якщо значення `serialized` не коректно.
-   Кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html) якщо властивості не коректні, наприклад, пропущені поля або вони мають некоректні значення.

### Дивіться також

-   [MongoDBDriverReadPreference::serialize()](mongodb-driver-readpreference.serialize.html) - Серіалізація ReadPreference
-   [unserialize()](function.unserialize.md) - Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
