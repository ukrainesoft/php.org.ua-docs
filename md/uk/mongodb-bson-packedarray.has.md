---
navigation:
  - mongodb-bson-packedarray.getiterator.md: '« MongoDB\\BSON\\PackedArray::getIterator'
  - mongodb-bson-packedarray.serialize.md: 'MongoDB\\BSON\\PackedArray::serialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-packedarray.md: MongoDB\\BSON\\PackedArray
title: 'MongoDB\\BSON\\PackedArray::has'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\PackedArray::has

(mongodb >=1.16.0)

MongoDB\\BSON\\PackedArray::has — Повертає, чи є індекс у масиві

### Опис

```methodsynopsis
final public MongoDB\BSON\PackedArray::has(int $index): bool
```

### Список параметрів

`index`(int)

Індекс, який слід шукати у масиві.

### Значення, що повертаються

Повертає **`true`**, якщо індекс присутній у масиві, інакше повертає значення **`false`**

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\BSON\\PackedArray::get()](mongodb-bson-packedarray.get.md) \- Повертає значення індексу масиву
-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
