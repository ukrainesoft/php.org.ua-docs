---
navigation:
  - mongodb-bson-symbol.tostring.html: '« MongoDBBSONSymbol::toString'
  - class.mongodb-bson-undefined.html: MongoDBBSONUndefined »
  - index.md: PHP Manual
  - class.mongodb-bson-symbol.html: MongoDBBSONSymbol
title: 'MongoDBBSONSymbol::unserialize'
---
# MongoDBBSONSymbol::unserialize

(mongodb >=1.4.0)

MongoDBBSONSymbol::unserialize — Десеріалізує Symbol

### Опис

```methodsynopsis
final public MongoDB\BSON\Symbol::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDBBSONSymbol](class.mongodb-bson-symbol.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBBSONSymbol::serialize()](mongodb-bson-symbol.serialize.md) - Серіалізує Symbol
-   [unserialize()](function.unserialize.md) - Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
