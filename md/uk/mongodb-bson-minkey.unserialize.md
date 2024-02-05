---
navigation:
  - mongodb-bson-minkey.serialize.md: '« MongoDB\\BSON\\MinKey::serialize'
  - class.mongodb-bson-objectid.md: MongoDB\\BSON\\ObjectId »
  - index.md: PHP Manual
  - class.mongodb-bson-minkey.md: MongoDB\\BSON\\MinKey
title: 'MongoDB\\BSON\\MinKey::unserialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\MinKey::unserialize

(mongodb >=1.2.0)

MongoDB\\BSON\\MonKey::unserialize — Серіалізує MonKey

### Опис

```methodsynopsis
final public MongoDB\BSON\MinKey::unserialize(string $data): void
```

### Список параметрів

`data`

Серіалізований [MongoDB\\BSON\\MinKey](class.mongodb-bson-minkey.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\BSON\\MinKey::serialize()](mongodb-bson-minkey.serialize.md) \- Серіалізує MinKey
-   [unserialize()](function.unserialize.md) \- Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
