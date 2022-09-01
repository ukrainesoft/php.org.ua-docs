---
navigation:
  - mongodb-driver-serverapi.serialize.html: '« MongoDBDriverServerApi::serialize'
  - class.mongodb-driver-writeconcern.html: MongoDBDriverWriteConcern »
  - index.html: PHP Manual
  - class.mongodb-driver-serverapi.html: MongoDBDriverServerApi
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

Серіалізований [MongoDBDriverServerApi](class.mongodb-driver-serverapi.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Викидає [MongoDBDriverExceptionUnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html)якщо властивості не можуть бути десеріалізовані (наприклад, `serialized` було некоректно сформовано).
-   Викидає [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)якщо властивості некоректні (наприклад, відсутні поля або містяться неприпустимі значення).

### Дивіться також

-   [MongoDBDriverServerApi::serialize()](mongodb-driver-serverapi.serialize.html) - Серіалізує ServerApi
-   [unserialize()](function.unserialize.html) - Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.html)
