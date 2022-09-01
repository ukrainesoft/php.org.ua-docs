---
navigation:
  - mongodb-driver-readpreference.gettagsets.html: '« MongoDBDriverReadPreference::getTagSets'
  - mongodb-driver-readpreference.unserialize.html: 'MongoDBDriverReadPreference::unserialize »'
  - index.md: PHP Manual
  - class.mongodb-driver-readpreference.html: MongoDBDriverReadPreference
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

Повертає серіалізовану виставу [MongoDBDriverReadPreference](class.mongodb-driver-readpreference.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverReadPreference::unserialize()](mongodb-driver-readpreference.unserialize.html) - Десеріалізація ReadPreference
-   [serialize()](function.serialize.md) - Генерує придатне для зберігання подання змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
