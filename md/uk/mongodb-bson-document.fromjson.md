---
navigation:
  - mongodb-bson-document.frombson.md: '« MongoDB\\BSON\\Document::fromBSON'
  - mongodb-bson-document.fromphp.md: 'MongoDB\\BSON\\Document::fromPHP »'
  - index.md: PHP Manual
  - class.mongodb-bson-document.md: MongoDB\\BSON\\Document
title: 'MongoDB\\BSON\\Document::fromJSON'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Document::fromJSON

(mongodb >=1.16.0)

MongoDB\\BSON\\Document::fromJSON — Створює новий екземпляр документа з рядка JSON

### Опис

```methodsynopsis
final static public MongoDB\BSON\Document::fromJSON(string $json): MongoDB\BSON\Document
```

Перетворює файл [» extended JSON](https://www.mongodb.com/docs/manual/reference/mongodb-extended-json/)в его BSON-представление.

### Список параметрів

`json`(string)

JSON-значення, яке підлягає перетворенню.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Викидає виняток [MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md), якщо параметр `json`не є коректним документом.

### Дивіться також

-   [MongoDB\\BSON\\Document::fromPHP()](mongodb-bson-document.fromphp.md) \- Створює новий екземпляр документа з даних PHP
-   [MongoDB\\BSON\\Document::fromBSON()](mongodb-bson-document.frombson.md) \- Створює новий екземпляр документа з BSON-рядку
-   [MongoDB\\BSON\\fromJSON()](function.mongodb.bson-fromjson.md) \- Повертає подання BSON значення JSON
-   [» MongoDB Extended JSON](https://www.mongodb.com/docs/manual/reference/mongodb-extended-json/)
-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
