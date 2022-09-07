---
navigation:
  - mongodb-bson-regex.jsonserialize.md: '« MongoDBBSONRegex::jsonSerialize'
  - mongodb-bson-regex.tostring.md: 'MongoDBBSONRegex::toString »'
  - index.md: PHP Manual
  - class.mongodb-bson-regex.md: MongoDBBSONRegex
title: 'MongoDBBSONRegex::serialize'
---
# MongoDBBSONRegex::serialize

(mongodb >=1.2.0)

MongoDBBSONRegex::serialize — Серіалізує Regex

### Опис

```methodsynopsis
final public MongoDB\BSON\Regex::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDBBSONRegex](class.mongodb-bson-regex.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBBSONRegex::unserialize()](mongodb-bson-regex.unserialize.md) - десеріалізує Regex
-   [serialize()](function.serialize.md) - Генерує придатне для зберігання уявлення змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
