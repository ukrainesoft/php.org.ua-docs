---
navigation:
  - mongodb-driver-cursorid.construct.html: '« MongoDBDriverCursorId::construct'
  - mongodb-driver-cursorid.tostring.html: 'MongoDBDriverCursorId::toString »'
  - index.html: PHP Manual
  - class.mongodb-driver-cursorid.html: MongoDBDriverCursorId
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

Повертає серіалізовану виставу [MongoDBDriverCursorId](class.mongodb-driver-cursorid.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverCursorId::unserialize()](mongodb-driver-cursorid.unserialize.html) - Десеріалізація CursorId
-   [serialize()](function.serialize.html) - Генерує придатне для зберігання подання змінної
-   [Серіалізація об'єктів](language.oop5.serialization.html)
