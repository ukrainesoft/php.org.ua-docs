---
navigation:
  - mongodb-bson-binary.tostring.html: '« MongoDBBSONBinary::toString'
  - class.mongodb-bson-decimal128.html: MongoDBBSONDecimal128 »
  - index.md: PHP Manual
  - class.mongodb-bson-binary.html: MongoDBBSONBinary
title: 'MongoDBBSONBinary::unserialize'
---
# MongoDBBSONBinary::unserialize

(mongodb >=1.2.0)

MongoDBBSONBinary::unserialize — Десеріалізує Binary

### Опис

```methodsynopsis
final public MongoDB\BSON\Binary::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDBBSONBinary](class.mongodb-bson-binary.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Видає [MongoDBDriverExceptionUnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html)якщо властивості не можуть бути десеріалізовані (наприклад, `serialized` був неправильно сформований).
-   Видає [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)якщо властивості неприпустимі (наприклад, відсутні поля або неприпустимі значення).

### Дивіться також

-   [MongoDBBSONBinary::serialize()](mongodb-bson-binary.serialize.html) - Серіалізує Binary
-   [unserialize()](function.unserialize.md) - Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
