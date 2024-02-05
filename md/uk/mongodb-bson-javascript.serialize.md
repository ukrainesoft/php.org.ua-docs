---
navigation:
  - mongodb-bson-javascript.jsonserialize.md: '« MongoDB\\BSON\\Javascript::jsonSerialize'
  - mongodb-bson-javascript.tostring.md: 'MongoDB\\BSON\\Javascript::\_\_toString »'
  - index.md: PHP Manual
  - class.mongodb-bson-javascript.md: MongoDB\\BSON\\Javascript
title: 'MongoDB\\BSON\\Javascript::serialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Javascript::serialize

(mongodb >=1.2.0)

MongoDB\\BSON\\Javascript::serialize — Серіалізувати JavaScript

### Опис

```methodsynopsis
final public MongoDB\BSON\Javascript::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Возвращает сериализованное представление[MongoDB\\BSON\\Javascript](class.mongodb-bson-javascript.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\BSON\\Javascript::unserialize()](mongodb-bson-javascript.unserialize.md) \- Десеріалізувати JavaScript
-   [serialize()](function.serialize.md) \- Генерує придатне для зберігання уявлення змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
