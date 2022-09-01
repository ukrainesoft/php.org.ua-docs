---
navigation:
  - mongodb-bson-timestamp.tostring.html: '« MongoDBBSONTimestamp::toString'
  - class.mongodb-bson-utcdatetime.html: MongoDBBSONUTCDateTime »
  - index.html: PHP Manual
  - class.mongodb-bson-timestamp.html: MongoDBBSONTimestamp
title: 'MongoDBBSONTimestamp::unserialize'
---
# MongoDBBSONTimestamp::unserialize

(mongodb >=1.2.0)

MongoDBBSONTimestamp::unserialize — Десеріалізує Timestamp

### Опис

```methodsynopsis
final public MongoDB\BSON\Timestamp::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDBBSONTimestamp](class.mongodb-bson-timestamp.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Видає [MongoDBDriverExceptionUnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html)якщо властивості не можуть бути не серіалізовані (наприклад, `serialized` був неправильно сформований).
-   Видає [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)якщо властивості неприпустимі (наприклад, відсутні поля або неприпустимі значення).

### Дивіться також

-   [MongoDBBSONTimestamp::serialize()](mongodb-bson-timestamp.serialize.html) - Серіалізує Timestamp
-   [unserialize()](function.unserialize.html) - Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.html)
