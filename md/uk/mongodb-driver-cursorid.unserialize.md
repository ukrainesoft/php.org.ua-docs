---
navigation:
  - mongodb-driver-cursorid.tostring.html: '« MongoDBDriverCursorId::toString'
  - class.mongodb-driver-cursorinterface.html: MongoDBDriverCursorInterface »
  - index.md: PHP Manual
  - class.mongodb-driver-cursorid.html: MongoDBDriverCursorId
title: 'MongoDBDriverCursorId::unserialize'
---
# MongoDBDriverCursorId::unserialize

(mongodb >=1.7.0)

MongoDBDriverCursorId::unserialize — Десеріалізація CursorId

### Опис

```methodsynopsis
final public MongoDB\Driver\CursorId::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDBDriverCursorId](class.mongodb-driver-cursorid.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Кидає виняток [MongoDBDriverExceptionUnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md) якщо виникла неможливо зробити десеріалізацію властивості, наприклад, якщо значення `serialized` не коректно.
-   Кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md) якщо властивості не коректні, наприклад, пропущені поля або вони мають некоректні значення.

### Дивіться також

-   [MongoDBDriverCursorId::serialize()](mongodb-driver-cursorid.serialize.md) - Серіалізація CursorId
-   [unserialize()](function.unserialize.md) - Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
