---
navigation:
  - mongodb-bson-document.get.md: '« MongoDB\\BSON\\Document::get'
  - mongodb-bson-document.has.md: 'MongoDB\\BSON\\Document::has »'
  - index.md: PHP Manual
  - class.mongodb-bson-document.md: MongoDB\\BSON\\Document
title: 'MongoDB\\BSON\\Document::getIterator'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Document::getIterator

(mongodb >=1.16.0)

MongoDB\\BSON\\Document::getIterator — Повертає ітератор для документа BSON

### Опис

```methodsynopsis
final public MongoDB\BSON\Document::getIterator(): MongoDB\BSON\Iterator
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає екземпляр [MongoDB\\BSON\\Iterator](class.mongodb-bson-iterator.md), який може бути використаний для ітерації на всі ключі в документі.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Викидає виняток [MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md)Якщо ітератор BSON не може бути ініціалізований.

### Дивіться також

-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
