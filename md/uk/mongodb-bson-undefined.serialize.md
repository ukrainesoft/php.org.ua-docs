---
navigation:
  - mongodb-bson-undefined.jsonserialize.md: '« MongoDB\\BSON\\Undefined::jsonSerialize'
  - mongodb-bson-undefined.tostring.md: 'MongoDB\\BSON\\Undefined::\_\_toString »'
  - index.md: PHP Manual
  - class.mongodb-bson-undefined.md: MongoDB\\BSON\\Undefined
title: 'MongoDB\\BSON\\Undefined::serialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Undefined::serialize

(mongodb >=1.4.0)

MongoDB\\BSON\\Undefined::serialize — Серіалізує Undefined

### Опис

```methodsynopsis
final public MongoDB\BSON\Undefined::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Возвращает сериализованное представление[MongoDB\\BSON\\Undefined](class.mongodb-bson-undefined.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\BSON\\Undefined::unserialize()](mongodb-bson-undefined.unserialize.md) \- Десеріалізує Undefined
-   [serialize()](function.serialize.md) \- Генерує придатне для зберігання уявлення змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
