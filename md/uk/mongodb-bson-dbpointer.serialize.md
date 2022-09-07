---
navigation:
  - mongodb-bson-dbpointer.jsonserialize.md: '« MongoDBBSONDBPointer::jsonSerialize'
  - mongodb-bson-dbpointer.tostring.md: 'MongoDBBSONDBPointer::toString »'
  - index.md: PHP Manual
  - class.mongodb-bson-dbpointer.md: MongoDBBSONDBPointer
title: 'MongoDBBSONDBPointer::serialize'
---
# MongoDBBSONDBPointer::serialize

(mongodb >=1.4.0)

MongoDBBSONDBPointer::serialize — Серіалізує DBPointer

### Опис

```methodsynopsis
final public MongoDB\BSON\DBPointer::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDBBSONDBPointer](class.mongodb-bson-dbpointer.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBBSONDBPointer::unserialize()](mongodb-bson-dbpointer.unserialize.md) - Десеріалізує DBPointer
-   [serialize()](function.serialize.md) - Генерує придатне для зберігання подання змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
