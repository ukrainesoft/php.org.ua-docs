---
navigation:
  - mongodb-driver-readpreference.gettagsets.md: '« MongoDB\\Driver\\ReadPreference::getTagSets'
  - mongodb-driver-readpreference.unserialize.md: 'MongoDB\\Driver\\ReadPreference::unserialize »'
  - index.md: PHP Manual
  - class.mongodb-driver-readpreference.md: MongoDB\\Driver\\ReadPreference
title: 'MongoDB\\Driver\\ReadPreference::serialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ReadPreference::serialize

(mongodb >=1.7.0)

MongoDB\\Driver\\ReadPreference::serialize — Серіалізація ReadPreference

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadPreference::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Возвращает сериализованное представление[MongoDB\\Driver\\ReadPreference](class.mongodb-driver-readpreference.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\ReadPreference::unserialize()](mongodb-driver-readpreference.unserialize.md) \- Десеріалізація ReadPreference
-   [serialize()](function.serialize.md) \- Генерує придатне для зберігання уявлення змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
