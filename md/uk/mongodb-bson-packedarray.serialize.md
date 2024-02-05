---
navigation:
  - mongodb-bson-packedarray.has.md: '« MongoDB\\BSON\\PackedArray::has'
  - mongodb-bson-packedarray.tophp.md: 'MongoDB\\BSON\\PackedArray::toPHP »'
  - index.md: PHP Manual
  - class.mongodb-bson-packedarray.md: MongoDB\\BSON\\PackedArray
title: 'MongoDB\\BSON\\PackedArray::serialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\PackedArray::serialize

(mongodb >=1.16.0)

MongoDB\\BSON\\PackedArray::serialize — Серіалізація масиву BSON

### Опис

```methodsynopsis
final public MongoDB\BSON\PackedArray::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Возвращает сериализованное представление массива[MongoDB\\BSON\\PackedArray](class.mongodb-bson-packedarray.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\BSON\\PackedArray::unserialize()](mongodb-bson-packedarray.unserialize.md) \- Десеріалізує масив BSON
-   [serialize()](function.serialize.md) \- Генерує придатне для зберігання уявлення змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
