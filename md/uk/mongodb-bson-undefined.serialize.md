---
navigation:
  - mongodb-bson-undefined.jsonserialize.html: '« MongoDBBSONUndefined::jsonSerialize'
  - mongodb-bson-undefined.tostring.html: 'MongoDBBSONUndefined::toString »'
  - index.md: PHP Manual
  - class.mongodb-bson-undefined.html: MongoDBBSONUndefined
title: 'MongoDBBSONUndefined::serialize'
---
# MongoDBBSONUndefined::serialize

(mongodb >=1.4.0)

MongoDBBSONUndefined::serialize — Серіалізує Undefined

### Опис

```methodsynopsis
final public MongoDB\BSON\Undefined::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDBBSONUndefined](class.mongodb-bson-undefined.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBBSONUndefined::unserialize()](mongodb-bson-undefined.unserialize.html) - Десеріалізує Undefined
-   [serialize()](function.serialize.md) - Генерує придатне для зберігання уявлення змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
