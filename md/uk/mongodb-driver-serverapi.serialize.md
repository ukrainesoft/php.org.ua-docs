---
navigation:
  - mongodb-driver-serverapi.construct.html: '« MongoDBDriverServerApi::construct'
  - mongodb-driver-serverapi.unserialize.html: 'MongoDBDriverServerApi::unserialize »'
  - index.md: PHP Manual
  - class.mongodb-driver-serverapi.html: MongoDBDriverServerApi
title: 'MongoDBDriverServerApi::serialize'
---
# MongoDBDriverServerApi::serialize

(mongodb >=1.10.0)

MongoDBDriverServerApi::serialize — Серіалізує ServerApi

### Опис

```methodsynopsis
final public MongoDB\Driver\ServerApi::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDBDriverServerApi](class.mongodb-driver-serverapi.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverServerApi::unserialize()](mongodb-driver-serverapi.unserialize.md) - Десеріалізує ServerApi
-   [serialize()](function.serialize.md) - Генерує придатне для зберігання уявлення змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
