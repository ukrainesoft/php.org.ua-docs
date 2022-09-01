---
navigation:
  - mongodb-bson-symbol.jsonserialize.html: '« MongoDBBSONSymbol::jsonSerialize'
  - mongodb-bson-symbol.tostring.html: 'MongoDBBSONSymbol::toString »'
  - index.md: PHP Manual
  - class.mongodb-bson-symbol.html: MongoDBBSONSymbol
title: 'MongoDBBSONSymbol::serialize'
---
# MongoDBBSONSymbol::serialize

(mongodb >=1.4.0)

MongoDBBSONSymbol::serialize — Серіалізує Symbol

### Опис

```methodsynopsis
final public MongoDB\BSON\Symbol::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовану виставу [MongoDBBSONSymbol](class.mongodb-bson-symbol.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBBSONSymbol::unserialize()](mongodb-bson-symbol.unserialize.md) - Десеріалізує Symbol
-   [serialize()](function.serialize.md) - Генерує придатне для зберігання подання змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
