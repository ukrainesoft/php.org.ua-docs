---
navigation:
  - mongodb-bson-regex.tostring.md: '« MongoDBBSONRegex::toString'
  - class.mongodb-bson-timestamp.md: MongoDBBSONTimestamp »
  - index.md: PHP Manual
  - class.mongodb-bson-regex.md: MongoDBBSONRegex
title: 'MongoDBBSONRegex::unserialize'
---
# MongoDBBSONRegex::unserialize

(mongodb >=1.2.0)

MongoDBBSONRegex::unserialize — Десеріалізує Regex

### Опис

```methodsynopsis
final public MongoDB\BSON\Regex::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDBBSONRegex](class.mongodb-bson-regex.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Видає [MongoDBDriverExceptionUnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md)якщо властивості не можуть бути не серіалізовані (наприклад, `serialized` був неправильно сформований).
-   Видає [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо властивості неприпустимі (наприклад, відсутні поля або неприпустимі значення).

### Дивіться також

-   [MongoDBBSONRegex::serialize()](mongodb-bson-regex.serialize.md) - Серіалізує Regex
-   [unserialize()](function.unserialize.md) - Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
