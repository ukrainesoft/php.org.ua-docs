---
navigation:
  - mongodb-driver-writeconcern.isdefault.html: '« MongoDBDriverWriteConcern::isDefault'
  - mongodb-driver-writeconcern.unserialize.html: 'MongoDBDriverWriteConcern::unserialize »'
  - index.md: PHP Manual
  - class.mongodb-driver-writeconcern.html: MongoDBDriverWriteConcern
title: 'MongoDBDriverWriteConcern::serialize'
---
# MongoDBDriverWriteConcern::serialize

(mongodb >=1.7.0)

MongoDBDriverWriteConcern::serialize — Серіалізація WriteConcern

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteConcern::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDBDriverWriteConcern](class.mongodb-driver-writeconcern.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverWriteConcern::unserialize()](mongodb-driver-writeconcern.unserialize.html) - Десеріалізація WriteConcern
-   [serialize()](function.serialize.md) - Генерує придатне для зберігання подання змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
