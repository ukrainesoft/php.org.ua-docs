---
navigation:
  - mongodb-bson-regex.jsonserialize.md: '« MongoDB\\BSON\\Regex::jsonSerialize'
  - mongodb-bson-regex.tostring.md: 'MongoDB\\BSON\\Regex::\_\_toString »'
  - index.md: PHP Manual
  - class.mongodb-bson-regex.md: MongoDB\\BSON\\Regex
title: 'MongoDB\\BSON\\Regex::serialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Regex::serialize

(mongodb >=1.2.0)

MongoDB\\BSON\\Regex::serialize — Серіалізує Regex

### Опис

```methodsynopsis
final public MongoDB\BSON\Regex::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Возвращает сериализованное представление[MongoDB\\BSON\\Regex](class.mongodb-bson-regex.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\BSON\\Regex::unserialize()](mongodb-bson-regex.unserialize.md) \- десеріалізує Regex
-   [serialize()](function.serialize.md) \- Генерує придатне для зберігання уявлення змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
