---
navigation:
  - mongodb-driver-readpreference.gettagsets.md: '« MongoDBDriverReadPreference::getTagSets'
  - mongodb-driver-readpreference.unserialize.md: 'MongoDBDriverReadPreference::unserialize »'
  - index.md: PHP Manual
  - class.mongodb-driver-readpreference.md: MongoDBDriverReadPreference
title: 'MongoDBDriverReadPreference::serialize'
---
# MongoDBDriverReadPreference::serialize

(mongodb >=1.7.0)

MongoDBDriverReadPreference::serialize — Серіалізація ReadPreference

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadPreference::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDBDriverReadPreference](class.mongodb-driver-readpreference.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverReadPreference::unserialize()](mongodb-driver-readpreference.unserialize.md) - Десеріалізація ReadPreference
-   [serialize()](function.serialize.md) - Генерує придатне для зберігання подання змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
