---
navigation:
  - mongodb-bson-document.fromphp.md: '« MongoDB\\BSON\\Document::fromPHP'
  - mongodb-bson-document.getiterator.md: 'MongoDB\\BSON\\Document::getIterator »'
  - index.md: PHP Manual
  - class.mongodb-bson-document.md: MongoDB\\BSON\\Document
title: 'MongoDB\\BSON\\Document::get'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Document::get

(mongodb >=1.16.0)

MongoDB\\BSON\\Document::get — Повертає значення ключа у документі

### Опис

```methodsynopsis
final public MongoDB\BSON\Document::get(string $key): mixed
```

### Список параметрів

`key`(string)

Ключ, який потрібно витягти з документа.

### Значення, що повертаються

Повертає значення, пов'язане із заданим ключем. Якщо ключ відсутній у документі, буде викинуто виняток.

> **Зауваження**: Якщо в BSON-документі зустрічається значення, закодоване як 64-бітове ціле число, то значенням цього методу, що повертається, буде екземпляр [MongoDB\\BSON\\Int64](class.mongodb-bson-int64.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Викидає виняток [MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.md), якщо ключ відсутній у документі.

### Дивіться також

-   [MongoDB\\BSON\\Document::has()](mongodb-bson-document.has.md) \- Повертає, чи є ключ у документі
-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
