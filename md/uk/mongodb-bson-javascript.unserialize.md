---
navigation:
  - mongodb-bson-javascript.tostring.md: '« MongoDB\\BSON\\Javascript::\_\_function toString() { [native code] }'
  - class.mongodb-bson-maxkey.md: MongoDB\\BSON\\MaxKey »
  - index.md: PHP Manual
  - class.mongodb-bson-javascript.md: MongoDB\\BSON\\Javascript
title: 'MongoDB\\BSON\\Javascript::unserialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Javascript::unserialize

(mongodb >=1.2.0)

MongoDB\\BSON\\Javascript::unserialize — Десеріалізувати JavaScript

### Опис

```methodsynopsis
final public MongoDB\BSON\Javascript::unserialize(string $data): void
```

### Список параметрів

`data`

Серіалізований [MongoDB\\BSON\\Javascript](class.mongodb-bson-javascript.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Викидає [MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md), если свойства не могут быть десериализованы (т.е . `serialized`неправильний).
-   Викидає [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md), якщо властивості некоректні (наприклад, відсутні поля чи неправильні неправильні значення).

### Дивіться також

-   [MongoDB\\BSON\\Javascript::serialize()](mongodb-bson-javascript.serialize.md) \- Серіалізувати JavaScript
-   [unserialize()](function.unserialize.md) \- Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
