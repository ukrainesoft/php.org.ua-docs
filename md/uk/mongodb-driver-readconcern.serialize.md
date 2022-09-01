---
navigation:
  - mongodb-driver-readconcern.isdefault.html: '« MongoDBDriverReadConcern::isDefault'
  - mongodb-driver-readconcern.unserialize.html: 'MongoDBDriverReadConcern::unserialize »'
  - index.md: PHP Manual
  - class.mongodb-driver-readconcern.html: MongoDBDriverReadConcern
title: 'MongoDBDriverReadConcern::serialize'
---
# MongoDBDriverReadConcern::serialize

(mongodb >=1.7.0)

MongoDBDriverReadConcern::serialize — Серіалізація ReadConcern

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadConcern::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDBDriverReadConcern](class.mongodb-driver-readconcern.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverReadConcern::unserialize()](mongodb-driver-readconcern.unserialize.md) - Десеріалізація ReadConcern
-   [serialize()](function.serialize.md) - Генерує придатне для зберігання подання змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
