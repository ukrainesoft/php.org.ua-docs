---
navigation:
  - mongodb-bson-packedarray.tostring.md: '« MongoDB\\BSON\\PackedArray::\_\_function toString() { [native code] }'
  - class.mongodb-bson-iterator.md: MongoDB\\BSON\\Iterator »
  - index.md: PHP Manual
  - class.mongodb-bson-packedarray.md: MongoDB\\BSON\\PackedArray
title: 'MongoDB\\BSON\\PackedArray::unserialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\PackedArray::unserialize

(mongodb >=1.16.0)

MongoDB\\BSON\\PackedArray::unserialize — Десеріалізує масив BSON

### Опис

```methodsynopsis
final public MongoDB\BSON\PackedArray::unserialize(string $data): void
```

### Список параметрів

`data`

Серіалізований [MongoDB\\BSON\\PackedArray](class.mongodb-bson-packedarray.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Викидає виняток [MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md), если свойства не могут быть десериализованы (т.е . `serialized`був неправильно сформований).
-   Викидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо властивості неприпустимі (наприклад, відсутні поля або неприпустимі значення).

### Дивіться також

-   [MongoDB\\BSON\\PackedArray::serialize()](mongodb-bson-packedarray.serialize.md) \- Серіалізація масиву BSON
-   [unserialize()](function.unserialize.md) \- Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
