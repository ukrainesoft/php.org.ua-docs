---
navigation:
  - mongodb-bson-dbpointer.tostring.md: '« MongoDB\\BSON\\DBPointer::\_\_function toString() { [native code] }'
  - class.mongodb-bson-int64.md: MongoDB\\BSON\\Int64 »
  - index.md: PHP Manual
  - class.mongodb-bson-dbpointer.md: MongoDB\\BSON\\DBPointer
title: 'MongoDB\\BSON\\DBPointer::unserialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\DBPointer::unserialize

(mongodb >=1.4.0)

MongoDB\\BSON\\DBPointer::unserialize — Десеріалізує DBPointer

### Опис

```methodsynopsis
final public MongoDB\BSON\DBPointer::unserialize(string $data): void
```

### Список параметрів

`data`

Серіалізований [MongoDB\\BSON\\DBPointer](class.mongodb-bson-dbpointer.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\BSON\\DBPointer::serialize()](mongodb-bson-dbpointer.serialize.md) \- Серіалізує DBPointer
-   [unserialize()](function.unserialize.md) \- Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
