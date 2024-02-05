---
navigation:
  - mongodb-bson-document.tostring.md: '« MongoDB\\BSON\\Document::\_\_function toString() { [native code] }'
  - class.mongodb-bson-packedarray.md: MongoDB\\BSON\\PackedArray »
  - index.md: PHP Manual
  - class.mongodb-bson-document.md: MongoDB\\BSON\\Document
title: 'MongoDB\\BSON\\Document::unserialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Document::unserialize

(mongodb >=1.16.0)

MongoDB\\BSON\\Document::unserialize — Десеріалізує BSON-документ

### Опис

```methodsynopsis
final public MongoDB\BSON\Document::unserialize(string $data): void
```

### Список параметрів

`data`

Серіалізований [MongoDB\\BSON\\Document](class.mongodb-bson-document.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Викидає виняток [MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md)якщо властивості не можуть бути десеріалізовані (наприклад, параметр`data`був неправильно сформований).
-   Викидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо властивості неприпустимі (наприклад, відсутні поля або неприпустимі значення).

### Дивіться також

-   [MongoDB\\BSON\\Document::serialize()](mongodb-bson-document.serialize.md) \- Серіалізує документ
-   [unserialize()](function.unserialize.md) \- Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
