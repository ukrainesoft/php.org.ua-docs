---
navigation:
  - mongodb-bson-dbpointer.jsonserialize.html: '« MongoDBBSONDBPointer::jsonSerialize'
  - mongodb-bson-dbpointer.tostring.html: 'MongoDBBSONDBPointer::toString »'
  - index.html: PHP Manual
  - class.mongodb-bson-dbpointer.html: MongoDBBSONDBPointer
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

Повертає серіалізовану виставу [MongoDBBSONDBPointer](class.mongodb-bson-dbpointer.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBBSONDBPointer::unserialize()](mongodb-bson-dbpointer.unserialize.html) - Десеріалізує DBPointer
-   [serialize()](function.serialize.html) - Генерує придатне для зберігання подання змінної
-   [Серіалізація об'єктів](language.oop5.serialization.html)
