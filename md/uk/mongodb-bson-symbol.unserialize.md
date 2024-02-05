---
navigation:
  - mongodb-bson-symbol.tostring.md: '« MongoDB\\BSON\\Symbol::\_\_function toString() { [native code] }'
  - class.mongodb-bson-undefined.md: MongoDB\\BSON\\Undefined »
  - index.md: PHP Manual
  - class.mongodb-bson-symbol.md: MongoDB\\BSON\\Symbol
title: 'MongoDB\\BSON\\Symbol::unserialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Symbol::unserialize

(mongodb >=1.4.0)

MongoDB\\BSON\\Symbol::unserialize — Десеріалізує Symbol

### Опис

```methodsynopsis
final public MongoDB\BSON\Symbol::unserialize(string $data): void
```

### Список параметрів

`data`

Серіалізований [MongoDB\\BSON\\Symbol](class.mongodb-bson-symbol.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\BSON\\Symbol::serialize()](mongodb-bson-symbol.serialize.md) \- Серіалізує Symbol
-   [unserialize()](function.unserialize.md) \- Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
