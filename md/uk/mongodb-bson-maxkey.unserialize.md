---
navigation:
  - mongodb-bson-maxkey.serialize.md: '« MongoDB\\BSON\\MaxKey::serialize'
  - class.mongodb-bson-minkey.md: MongoDB\\BSON\\MinKey »
  - index.md: PHP Manual
  - class.mongodb-bson-maxkey.md: MongoDB\\BSON\\MaxKey
title: 'MongoDB\\BSON\\MaxKey::unserialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\MaxKey::unserialize

(mongodb >=1.2.0)

MongoDB\\BSON\\MaxKey::unserialize — Десеріалізує MaxKey

### Опис

```methodsynopsis
final public MongoDB\BSON\MaxKey::unserialize(string $data): void
```

### Список параметрів

`data`

Серіалізований [MongoDB\\BSON\\MaxKey](class.mongodb-bson-maxkey.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\BSON\\MaxKey::serialize()](mongodb-bson-maxkey.serialize.md) \- Серіалізує MaxKey
-   [unserialize()](function.unserialize.md) \- Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
