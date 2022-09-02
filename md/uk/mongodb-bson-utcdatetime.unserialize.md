---
navigation:
  - mongodb-bson-utcdatetime.tostring.md: '« MongoDBBSONUTCDateTime::toString'
  - class.mongodb-bson-type.md: MongoDBBSONType »
  - index.md: PHP Manual
  - class.mongodb-bson-utcdatetime.md: MongoDBBSONUTCDateTime
title: 'MongoDBBSONUTCDateTime::unserialize'
---
# MongoDBBSONUTCDateTime::unserialize

(mongodb >=1.2.0)

MongoDBBSONUTCDateTime::unserialize — Десеріалізує UTCDateTime

### Опис

```methodsynopsis
final public MongoDB\BSON\UTCDateTime::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDBBSONUTCDateTime](class.mongodb-bson-utcdatetime.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Видає [MongoDBDriverExceptionUnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md)якщо властивості не можуть бути не серіалізовані (наприклад, `serialized` був неправильно сформований).
-   Видає [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо властивості неприпустимі (наприклад, відсутні поля або неприпустимі значення).

### Дивіться також

-   [MongoDBBSONUTCDateTime::serialize()](mongodb-bson-utcdatetime.serialize.md) - Серіалізує UTCDateTime
-   [unserialize()](function.unserialize.md) - Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
