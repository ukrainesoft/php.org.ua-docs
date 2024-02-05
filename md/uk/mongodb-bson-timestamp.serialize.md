---
navigation:
  - mongodb-bson-timestamp.jsonserialize.md: '« MongoDB\\BSON\\Timestamp::jsonSerialize'
  - mongodb-bson-timestamp.tostring.md: 'MongoDB\\BSON\\Timestamp::\_\_toString »'
  - index.md: PHP Manual
  - class.mongodb-bson-timestamp.md: MongoDB\\BSON\\Timestamp
title: 'MongoDB\\BSON\\Timestamp::serialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Timestamp::serialize

(mongodb >=1.2.0)

MongoDB\\BSON\\Timestamp::serialize — Серіалізує Timestamp

### Опис

```methodsynopsis
final public MongoDB\BSON\Timestamp::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Возвращает сериализованное представление[MongoDB\\BSON\\Timestamp](class.mongodb-bson-timestamp.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\BSON\\Timestamp::unserialize()](mongodb-bson-timestamp.unserialize.md) \- Десеріалізує Timestamp
-   [serialize()](function.serialize.md) \- Генерує придатне для зберігання уявлення змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
