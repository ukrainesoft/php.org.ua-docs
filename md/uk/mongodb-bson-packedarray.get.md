---
navigation:
  - mongodb-bson-packedarray.fromphp.md: '« MongoDB\\BSON\\PackedArray::fromPHP'
  - mongodb-bson-packedarray.getiterator.md: 'MongoDB\\BSON\\PackedArray::getIterator »'
  - index.md: PHP Manual
  - class.mongodb-bson-packedarray.md: MongoDB\\BSON\\PackedArray
title: 'MongoDB\\BSON\\PackedArray::get'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\PackedArray::get

(mongodb >=1.16.0)

MongoDB\\BSON\\PackedArray::get — Повертає значення індексу масиву

### Опис

```methodsynopsis
final public MongoDB\BSON\PackedArray::get(int $key): mixed
```

### Список параметрів

`key`(int)

Індекс для отримання масиву.

### Значення, що повертаються

Повертає значення, пов'язане із заданим індексом. Якщо індекс не є у документі, то буде викинуто виняток.

> **Зауваження**: Якщо в масиві BSON зустрічається значення, закодоване як 64-бітове ціле число, то значенням методу, що повертається, буде екземпляр [MongoDB\\BSON\\Int64](class.mongodb-bson-int64.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Викидає виняток [MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.md)якщо індекс відсутній у масиві.

### Дивіться також

-   [MongoDB\\BSON\\PackedArray::has()](mongodb-bson-packedarray.has.md) \- Повертає, чи є індекс у масиві
-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
