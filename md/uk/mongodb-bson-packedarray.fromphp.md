---
navigation:
  - mongodb-bson-packedarray.construct.md: '« MongoDB\\BSON\\PackedArray::\_\_construct'
  - mongodb-bson-packedarray.get.md: 'MongoDB\\BSON\\PackedArray::get »'
  - index.md: PHP Manual
  - class.mongodb-bson-packedarray.md: MongoDB\\BSON\\PackedArray
title: 'MongoDB\\BSON\\PackedArray::fromPHP'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\PackedArray::fromPHP

(mongodb >=1.16.0)

MongoDB\\BSON\\PackedArray::fromPHP — Створює новий екземпляр масиву BSON з даних PHP

### Опис

```methodsynopsis
final static public MongoDB\BSON\PackedArray::fromPHP(array $value): MongoDB\BSON\PackedArray
```

### Список параметрів

`value`(array)

Масив PHP для перетворення на масив BSON. Масив повинен бути списком (тобто мати послідовні числові ключі, що починаються з

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Викидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо заданий масив не є списком (тобто має послідовні числові ключі, що починаються з

### Дивіться також

-   [MongoDB\\BSON\\fromPHP()](function.mongodb.bson-fromphp.md) \- Повертає представлення BSON значення PHP
-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
