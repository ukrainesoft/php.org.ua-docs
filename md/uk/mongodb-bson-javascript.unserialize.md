---
navigation:
  - mongodb-bson-javascript.tostring.md: '« MongoDBBSONJavascript::toString'
  - class.mongodb-bson-maxkey.md: MongoDBBSONMaxKey »
  - index.md: PHP Manual
  - class.mongodb-bson-javascript.md: MongoDBBSONJavascript
title: 'MongoDBBSONJavascript::unserialize'
---
# MongoDBBSONJavascript::unserialize

(mongodb >=1.2.0)

MongoDBBSONJavascript::unserialize — Десеріалізувати JavaScript

### Опис

```methodsynopsis
final public MongoDB\BSON\Javascript::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDBBSONJavascript](class.mongodb-bson-javascript.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Викидає [MongoDBDriverExceptionUnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md)якщо властивості не можуть бути десеріалізовані (тобто . `serialized` неправильний).
-   Викидає [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md), якщо властивості некоректні (наприклад, відсутні поля чи неправильні неправильні значення).

### Дивіться також

-   [MongoDBBSONJavascript::serialize()](mongodb-bson-javascript.serialize.md) - Серіалізувати JavaScript
-   [unserialize()](function.unserialize.md) - Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
