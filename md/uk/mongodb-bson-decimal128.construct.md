---
navigation:
  - class.mongodb-bson-decimal128.md: « MongoDB\\BSON\\Decimal128
  - mongodb-bson-decimal128.jsonserialize.md: 'MongoDB\\BSON\\Decimal128::jsonSerialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-decimal128.md: MongoDB\\BSON\\Decimal128
title: 'MongoDB\\BSON\\Decimal128::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Decimal128::\_\_construct

(mongodb >=1.2.0)

MongoDB\\BSON\\Decimal128::\_\_construct — Створює новий Decimal128

### Опис

```methodsynopsis
final public MongoDB\BSON\Decimal128::__construct(string $value)
```

> **Зауваження** [MongoDB\\BSON\\Decimal128](class.mongodb-bson-decimal128.md) сумісний лише з MongoDB 3.4+. При спробі використовувати тип BSON з попередніми версіями приведе до помилки.

### Список параметрів

`value`(string)

Десятковий рядок.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Видає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md), якщо `value`не є допустимим десятковим рядком.

### Приклади

**Приклад #1 Приклад використання** MongoDB\\BSON\\Decimal128::\_\_construct()\*\*\*\*

```php
<?php

var_dump(new MongoDB\BSON\Decimal128(1234.5678));
var_dump(new MongoDB\BSON\Decimal128(NAN));
var_dump(new MongoDB\BSON\Decimal128(INF));

?>
```

Висновок наведеного прикладу буде схожим на:

```
object(MongoDB\BSON\Decimal128)#1 (1) {
  ["dec"]=>
  string(9) "1234.5678"
}
object(MongoDB\BSON\Decimal128)#1 (1) {
  ["dec"]=>
  string(3) "NaN"
}
object(MongoDB\BSON\Decimal128)#1 (1) {
  ["dec"]=>
  string(8) "Infinity"
}
```

### Дивіться також

-   [» Формат з плаваючою точкою Decimal128](https://en.wikipedia.org/wiki/Decimal128_floating-point_format)
-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
