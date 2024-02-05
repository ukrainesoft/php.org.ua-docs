---
navigation:
  - mongodb-bson-document.has.md: '« MongoDB\\BSON\\Document::has'
  - mongodb-bson-document.tocanonicalextendedjson.md: 'MongoDB\\BSON\\Document::toCanonicalExtendedJSON »'
  - index.md: PHP Manual
  - class.mongodb-bson-document.md: MongoDB\\BSON\\Document
title: 'MongoDB\\BSON\\Document::serialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Document::serialize

(mongodb >=1.16.0)

MongoDB\\BSON\\Document::serialize — Серіалізує документ

### Опис

```methodsynopsis
final public MongoDB\BSON\Document::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Возвращает сериализованное представление[MongoDB\\BSON\\Document](class.mongodb-bson-document.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\BSON\\Document::unserialize()](mongodb-bson-document.unserialize.md) \- Десеріалізує BSON-документ
-   [serialize()](function.serialize.md) \- Генерує придатне для зберігання уявлення змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
