---
navigation:
  - mongodb-bson-document.getiterator.md: '« MongoDB\\BSON\\Document::getIterator'
  - mongodb-bson-document.serialize.md: 'MongoDB\\BSON\\Document::serialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-document.md: MongoDB\\BSON\\Document
title: 'MongoDB\\BSON\\Document::has'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Document::has

(mongodb >=1.16.0)

MongoDB\\BSON\\Document::has — Повертає, чи є ключ у документі

### Опис

```methodsynopsis
final public MongoDB\BSON\Document::has(string $key): bool
```

### Список параметрів

`key`(string)

Ключ, який потрібно шукати в документі.

### Значення, що повертаються

Повертає **`true`**, якщо ключ присутній у документі, інакше повертає **`false`**

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\BSON\\Document::get()](mongodb-bson-document.get.md) \- Повертає значення ключа у документі
-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
