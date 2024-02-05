---
navigation:
  - mongodb-bson-packedarray.get.md: '« MongoDB\\BSON\\PackedArray::get'
  - mongodb-bson-packedarray.has.md: 'MongoDB\\BSON\\PackedArray::has »'
  - index.md: PHP Manual
  - class.mongodb-bson-packedarray.md: MongoDB\\BSON\\PackedArray
title: 'MongoDB\\BSON\\PackedArray::getIterator'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\PackedArray::getIterator

(mongodb >=1.16.0)

MongoDB\\BSON\\PackedArray::getIterator — Повертає ітератор для масиву BSON

### Опис

```methodsynopsis
final public MongoDB\BSON\PackedArray::getIterator(): MongoDB\BSON\Iterator
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає екземпляр [MongoDB\\BSON\\Iterator](class.mongodb-bson-iterator.md), який може бути використаний для ітерації по всіх індексах масиву.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Викидає виняток [MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md)Якщо ітератор BSON не може бути ініціалізований.

### Дивіться також

-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
