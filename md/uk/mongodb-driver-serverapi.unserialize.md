---
navigation:
  - mongodb-driver-serverapi.serialize.md: '« MongoDBDriverServerApi::serialize'
  - class.mongodb-driver-writeconcern.md: MongoDBDriverWriteConcern »
  - index.md: PHP Manual
  - class.mongodb-driver-serverapi.md: MongoDBDriverServerApi
title: 'MongoDBDriverServerApi::unserialize'
---
# MongoDBDriverServerApi::unserialize

(mongodb >=1.10.0)

MongoDBDriverServerApi::unserialize — Десеріалізує ServerApi

### Опис

```methodsynopsis
final public MongoDB\Driver\ServerApi::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDBDriverServerApi](class.mongodb-driver-serverapi.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Викидає [MongoDBDriverExceptionUnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md)якщо властивості не можуть бути десеріалізовані (наприклад, `serialized` було некоректно сформовано).
-   Викидає [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо властивості некоректні (наприклад, відсутні поля або містяться неприпустимі значення).

### Дивіться також

-   [MongoDBDriverServerApi::serialize()](mongodb-driver-serverapi.serialize.md) - Серіалізує ServerApi
-   [unserialize()](function.unserialize.md) - Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
