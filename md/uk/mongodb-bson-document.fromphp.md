---
navigation:
  - mongodb-bson-document.fromjson.md: '« MongoDB\\BSON\\Document::fromJSON'
  - mongodb-bson-document.get.md: 'MongoDB\\BSON\\Document::get »'
  - index.md: PHP Manual
  - class.mongodb-bson-document.md: MongoDB\\BSON\\Document
title: 'MongoDB\\BSON\\Document::fromPHP'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Document::fromPHP

(mongodb >=1.16.0)

MongoDB\\BSON\\Document::from PHP — Створює новий екземпляр документа з даних PHP

### Опис

```methodsynopsis
final static public MongoDB\BSON\Document::fromPHP(object|array $value): MongoDB\BSON\Document
```

### Список параметрів

`value`(object|array)

PHP-об'єкт чи масив, що містить документ. При передачі масиву з числовими ключами числові значення перетворюються на рядки і використовуються як ключі документа.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\BSON\\Document::fromBSON()](mongodb-bson-document.frombson.md) \- Створює новий екземпляр документа з BSON-рядку
-   [MongoDB\\BSON\\Document::fromJSON()](mongodb-bson-document.fromjson.md) \- Створює новий екземпляр документа з рядка JSON
-   [MongoDB\\BSON\\fromPHP()](function.mongodb.bson-fromphp.md) \- Повертає представлення BSON значення PHP
-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
