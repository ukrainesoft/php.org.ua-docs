---
navigation:
  - mongodb-bson-packedarray.serialize.md: '« MongoDB\\BSON\\PackedArray::serialize'
  - mongodb-bson-packedarray.tostring.md: 'MongoDB\\BSON\\PackedArray::\_\_toString »'
  - index.md: PHP Manual
  - class.mongodb-bson-packedarray.md: MongoDB\\BSON\\PackedArray
title: 'MongoDB\\BSON\\PackedArray::toPHP'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\PackedArray::toPHP

(mongodb >=1.16.0)

MongoDB\\BSON\\PackedArray::toPHP — Повертає PHP-подання масиву BSON

### Опис

```methodsynopsis
final public MongoDB\BSON\PackedArray::toPHP(?array $typeMap = null): array|object
```

### Список параметрів

`typeMap`(array)

[Конфігурація карти типів](mongodb.persistence.deserialization.md#mongodb.persistence.typemaps)

### Значення, що повертаються

Декодоване значення PHP.

> **Зауваження**: Якщо в масиві BSON зустрічається значення, закодоване як 64-бітове ціле число, то значенням методу, що повертається, буде екземпляр [MongoDB\\BSON\\Int64](class.mongodb-bson-int64.md)

### Помилки

-   Викидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо клас у карті типів не може бути ініціалізований або не реалізує інтерфейс[MongoDB\\BSON\\Unserializable](class.mongodb-bson-unserializable.md)

### Дивіться також

-   [MongoDB\\BSON\\toPHP()](function.mongodb.bson-tophp.md) \- Повертає PHP подання значення BSON
-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
