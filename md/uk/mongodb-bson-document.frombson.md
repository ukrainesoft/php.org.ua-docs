---
navigation:
  - mongodb-bson-document.construct.md: '« MongoDB\\BSON\\Document::\_\_construct'
  - mongodb-bson-document.fromjson.md: 'MongoDB\\BSON\\Document::fromJSON »'
  - index.md: PHP Manual
  - class.mongodb-bson-document.md: MongoDB\\BSON\\Document
title: 'MongoDB\\BSON\\Document::fromBSON'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Document::fromBSON

(mongodb >=1.16.0)

MongoDB\\BSON\\Document::fromBSON — Створює новий екземпляр документа з BSON-рядку

### Опис

```methodsynopsis
final static public MongoDB\BSON\Document::fromBSON(string $bson): MongoDB\BSON\Document
```

### Список параметрів

`bson`(string)

Рядок, що містить документ у форматі BSON.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Викидає [MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md), якщо параметр `bson`є некоректним BSON-рядком або містить більше одного документа.

### Дивіться також

-   [MongoDB\\BSON\\Document::fromPHP()](mongodb-bson-document.fromphp.md) \- Створює новий екземпляр документа з даних PHP
-   [MongoDB\\BSON\\Document::fromJSON()](mongodb-bson-document.fromjson.md) \- Створює новий екземпляр документа з рядка JSON
-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
