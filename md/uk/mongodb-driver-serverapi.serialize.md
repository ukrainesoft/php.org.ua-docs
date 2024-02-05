---
navigation:
  - mongodb-driver-serverapi.construct.md: '« MongoDB\\Driver\\ServerApi::\_\_construct'
  - mongodb-driver-serverapi.unserialize.md: 'MongoDB\\Driver\\ServerApi::unserialize »'
  - index.md: PHP Manual
  - class.mongodb-driver-serverapi.md: MongoDB\\Driver\\ServerApi
title: 'MongoDB\\Driver\\ServerApi::serialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ServerApi::serialize

(mongodb >=1.10.0)

MongoDB\\Driver\\ServerApi::serialize — Серіалізує ServerApi

### Опис

```methodsynopsis
final public MongoDB\Driver\ServerApi::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Возвращает сериализованное представление[MongoDB\\Driver\\ServerApi](class.mongodb-driver-serverapi.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\ServerApi::unserialize()](mongodb-driver-serverapi.unserialize.md) \- Десеріалізує ServerApi
-   [serialize()](function.serialize.md) \- Генерує придатне для зберігання уявлення змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
