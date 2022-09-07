---
navigation:
  - mongodb-driver-cursorid.construct.md: '« MongoDBDriverCursorId::construct'
  - mongodb-driver-cursorid.tostring.md: 'MongoDBDriverCursorId::toString »'
  - index.md: PHP Manual
  - class.mongodb-driver-cursorid.md: MongoDBDriverCursorId
title: 'MongoDBDriverCursorId::serialize'
---
# MongoDBDriverCursorId::serialize

(mongodb >=1.7.0)

MongoDBDriverCursorId::serialize — Серіалізація CursorId

### Опис

```methodsynopsis
final public MongoDB\Driver\CursorId::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDBDriverCursorId](class.mongodb-driver-cursorid.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverCursorId::unserialize()](mongodb-driver-cursorid.unserialize.md) - Десеріалізація CursorId
-   [serialize()](function.serialize.md) - Генерує придатне для зберігання подання змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
