---
navigation:
  - mongodb-bson-int64.jsonserialize.md: '« MongoDB\\BSON\\Int64::jsonSerialize'
  - mongodb-bson-int64.tostring.md: 'MongoDB\\BSON\\Int64::\_\_toString »'
  - index.md: PHP Manual
  - class.mongodb-bson-int64.md: MongoDB\\BSON\\Int64
title: 'MongoDB\\BSON\\Int64::serialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Int64::serialize

(mongodb >=1.5.0)

MongoDB\\BSON\\Int64::serialize — Серіалізує Int64

### Опис

```methodsynopsis
final public MongoDB\BSON\Int64::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Возвращает сериализованное представление[MongoDB\\BSON\\Int64](class.mongodb-bson-int64.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\BSON\\Int64::unserialize()](mongodb-bson-int64.unserialize.md) \- Десеріалізує Int64
-   [serialize()](function.serialize.md) \- Генерує придатне для зберігання уявлення змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
