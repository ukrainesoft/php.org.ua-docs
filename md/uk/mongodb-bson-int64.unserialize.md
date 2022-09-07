---
navigation:
  - mongodb-bson-int64.tostring.md: '« MongoDBBSONInt64::toString'
  - class.mongodb-bson-symbol.md: MongoDBBSONSymbol »
  - index.md: PHP Manual
  - class.mongodb-bson-int64.md: MongoDBBSONInt64
title: 'MongoDBBSONInt64::unserialize'
---
# MongoDBBSONInt64::unserialize

(mongodb >=1.5.0)

MongoDBBSONInt64::unserialize — Десеріалізує Int64

### Опис

```methodsynopsis
final public MongoDB\BSON\Int64::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDBBSONInt64](class.mongodb-bson-int64.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Видає виняток [MongoDBDriverExceptionUnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md)якщо властивості не можуть бути не серіалізовані (тобто `serialized` був неправильно сформований).
-   Видає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо властивості неприпустимі (наприклад, відсутні поля або неприпустимі значення).

### Дивіться також

-   [MongoDBBSONInt64::serialize()](mongodb-bson-int64.serialize.md) - Серіалізує Int64
-   [unserialize()](function.unserialize.md) - Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
