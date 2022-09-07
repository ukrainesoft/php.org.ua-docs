---
navigation:
  - mongodb-bson-maxkey.jsonserialize.md: '« MongoDBBSONMaxKey::jsonSerialize'
  - mongodb-bson-maxkey.unserialize.md: 'MongoDBBSONMaxKey::unserialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-maxkey.md: MongoDBBSONMaxKey
title: 'MongoDBBSONMaxKey::serialize'
---
# MongoDBBSONMaxKey::serialize

(mongodb >=1.2.0)

MongoDBBSONMaxKey::serialize — Серіалізує MaxKey

### Опис

```methodsynopsis
final public MongoDB\BSON\MaxKey::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDBBSONMaxKey](class.mongodb-bson-maxkey.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBBSONMaxKey::unserialize()](mongodb-bson-maxkey.unserialize.md) - Десеріалізує MaxKey
-   [serialize()](function.serialize.md) - Генерує придатне для зберігання уявлення змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
