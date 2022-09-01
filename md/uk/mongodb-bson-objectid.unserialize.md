---
navigation:
  - mongodb-bson-objectid.tostring.html: '« MongoDBBSONObjectId::toString'
  - class.mongodb-bson-regex.html: MongoDBBSONRegex »
  - index.md: PHP Manual
  - class.mongodb-bson-objectid.html: MongoDBBSONObjectId
title: 'MongoDBBSONObjectId::unserialize'
---
# MongoDBBSONObjectId::unserialize

(mongodb >=1.2.0)

MongoDBBSONObjectId::unserialize — Десеріалізує ObjectId

### Опис

```methodsynopsis
final public MongoDB\BSON\ObjectId::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDBBSONObjectId](class.mongodb-bson-objectid.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Видає виняток [MongoDBDriverExceptionUnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md)якщо властивості не можуть бути десеріалізовані (наприклад, `serialized` був неправильно сформований).
-   Видає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо властивості недійсні (наприклад, відсутні поля або неприпустимі значення).

### Дивіться також

-   [MongoDBBSONObjectId::serialize()](mongodb-bson-objectid.serialize.md) - Серіалізує ObjectId
-   [unserialize()](function.unserialize.md) - Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
