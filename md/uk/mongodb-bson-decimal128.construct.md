Створює новий Decimal128

-   [« MongoDBBSONDecimal128](class.mongodb-bson-decimal128.html)
    
-   [MongoDBBSONDecimal128::jsonSerialize »](mongodb-bson-decimal128.jsonserialize.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBBSONDecimal128](class.mongodb-bson-decimal128.html)
    
-   Створює новий Decimal128
    

# MongoDBBSONDecimal128::construct

(mongodb >=1.2.0)

MongoDBBSONDecimal128::construct — Створює новий Decimal128

### Опис

```methodsynopsis
final public MongoDB\BSON\Decimal128::__construct(string $value)
```

> **Зауваження** [MongoDBBSONDecimal128](class.mongodb-bson-decimal128.html) сумісний лише з MongoDB 3.4+. При спробі використовувати тип BSON з попередніми версіями приведе до помилки.

### Список параметрів

`value` (string)

Десятковий рядок.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Видає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html), якщо `value` не є допустимим десятковим рядком.

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONDecimal128::construct()****

```php
<?php

var_dump(new MongoDB\BSON\Decimal128(1234.5678));
var_dump(new MongoDB\BSON\Decimal128(NAN));
var_dump(new MongoDB\BSON\Decimal128(INF));

?>
```

Результатом виконання цього прикладу буде щось подібне:

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