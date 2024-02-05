---
navigation:
  - class.mongodb-bson-iterator.md: « MongoDB\\BSON\\Iterator
  - mongodb-bson-iterator.current.md: 'MongoDB\\BSON\\Iterator::current »'
  - index.md: PHP Manual
  - class.mongodb-bson-iterator.md: MongoDB\\BSON\\Iterator
title: 'MongoDB\\BSON\\Iterator::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Iterator::\_\_construct

(No version information available, might only be in Git)

MongoDB\\BSON\\Iterator::\_\_construct — Створює новий ітератор BSON (не використовується)

### Опис

```methodsynopsis
final private MongoDB\BSON\Iterator::__construct()
```

Об'єкти [MongoDB\\BSON\\Iterator](class.mongodb-bson-iterator.md) створюються шляхом виклику [MongoDB\\BSON\\Document::getIterator()](mongodb-bson-document.getiterator.md) або [MongoDB\\BSON\\PackedArray::getIterator()](mongodb-bson-packedarray.getiterator.md) і не можуть бути ініціалізовані безпосередньо.

### Список параметрів

Ця функція не має параметрів.

### Дивіться також

-   [MongoDB\\BSON\\Document::getIterator()](mongodb-bson-document.getiterator.md) \- Повертає ітератор для документа BSON
-   [MongoDB\\BSON\\PackedArray::getIterator()](mongodb-bson-packedarray.getiterator.md) \- Повертає ітератор для масиву BSON
-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
