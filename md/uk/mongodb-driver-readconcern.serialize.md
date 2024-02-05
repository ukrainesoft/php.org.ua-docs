---
navigation:
  - mongodb-driver-readconcern.isdefault.md: '« MongoDB\\Driver\\ReadConcern::isDefault'
  - mongodb-driver-readconcern.unserialize.md: 'MongoDB\\Driver\\ReadConcern::unserialize »'
  - index.md: PHP Manual
  - class.mongodb-driver-readconcern.md: MongoDB\\Driver\\ReadConcern
title: 'MongoDB\\Driver\\ReadConcern::serialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ReadConcern::serialize

(mongodb >=1.7.0)

MongoDB\\Driver\\ReadConcern::serialize — Серіалізація ReadConcern

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadConcern::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Возвращает сериализованное представление[MongoDB\\Driver\\ReadConcern](class.mongodb-driver-readconcern.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\ReadConcern::unserialize()](mongodb-driver-readconcern.unserialize.md) \- Десеріалізація ReadConcern
-   [serialize()](function.serialize.md) \- Генерує придатне для зберігання уявлення змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
