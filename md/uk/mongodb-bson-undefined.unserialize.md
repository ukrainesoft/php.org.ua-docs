---
navigation:
  - mongodb-bson-undefined.tostring.md: '« MongoDB\\BSON\\Undefined::\_\_function toString() { [native code] }'
  - mongodb.monitoring.md: MongoDB\\Driver\\Monitoring »
  - index.md: PHP Manual
  - class.mongodb-bson-undefined.md: MongoDB\\BSON\\Undefined
title: 'MongoDB\\BSON\\Undefined::unserialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Undefined::unserialize

(mongodb >=1.4.0)

MongoDB\\BSON\\Undefined::unserialize — Десеріалізує Undefined

### Опис

```methodsynopsis
final public MongoDB\BSON\Undefined::unserialize(string $data): void
```

### Список параметрів

`data`

Серіалізований [MongoDB\\BSON\\Undefined](class.mongodb-bson-undefined.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\BSON\\Undefined::serialize()](mongodb-bson-undefined.serialize.md) \- Серіалізує Undefined
-   [unserialize()](function.unserialize.md) \- Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
