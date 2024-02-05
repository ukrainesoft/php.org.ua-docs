---
navigation:
  - mongodb-driver-writeconcern.isdefault.md: '« MongoDB\\Driver\\WriteConcern::isDefault'
  - mongodb-driver-writeconcern.unserialize.md: 'MongoDB\\Driver\\WriteConcern::unserialize »'
  - index.md: PHP Manual
  - class.mongodb-driver-writeconcern.md: MongoDB\\Driver\\WriteConcern
title: 'MongoDB\\Driver\\WriteConcern::serialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\WriteConcern::serialize

(mongodb >=1.7.0)

MongoDB\\Driver\\WriteConcern::serialize — Серіалізація WriteConcern

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteConcern::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Возвращает сериализованное представление[MongoDB\\Driver\\WriteConcern](class.mongodb-driver-writeconcern.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\WriteConcern::unserialize()](mongodb-driver-writeconcern.unserialize.md) \- Десеріалізація WriteConcern
-   [serialize()](function.serialize.md) \- Генерує придатне для зберігання уявлення змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
