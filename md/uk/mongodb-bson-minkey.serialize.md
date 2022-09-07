---
navigation:
  - mongodb-bson-minkey.jsonserialize.md: '« MongoDBBSONMinKey::jsonSerialize'
  - mongodb-bson-minkey.unserialize.md: 'MongoDBBSONMinKey::unserialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-minkey.md: MongoDBBSONMinKey
title: 'MongoDBBSONMinKey::serialize'
---
# MongoDBBSONMinKey::serialize

(mongodb >=1.2.0)

MongoDBBSONMonKey::serialize — Серіалізує MonKey

### Опис

```methodsynopsis
final public MongoDB\BSON\MinKey::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDBBSONMinKey](class.mongodb-bson-minkey.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBBSONMinKey::unserialize()](mongodb-bson-minkey.unserialize.md) - Десеріалізує MinKey
-   [serialize()](function.serialize.md) - Генерує придатне для зберігання подання змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
