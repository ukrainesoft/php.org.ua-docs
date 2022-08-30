Повертає рядкову виставу Decimal128

-   [« MongoDBBSONDecimal128::serialize](mongodb-bson-decimal128.serialize.html)
    
-   [MongoDBBSONDecimal128::unserialize »](mongodb-bson-decimal128.unserialize.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBBSONDecimal128](class.mongodb-bson-decimal128.html)
    
-   Повертає рядкову виставу Decimal128
    

# MongoDBBSONDecimal128::function toString() { \[native code\] }

(mongodb >=1.2.0)

MongoDBBSONDecimal128::toString — Повертає рядкову виставу Decimal128

### Опис

```methodsynopsis
final public MongoDB\BSON\Decimal128::__toString(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядкову виставу Decimal128.

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONDecimal128::toString()****

```php
<?php

var_dump((string) new MongoDB\BSON\Decimal128(1234.5678));
var_dump((string) new MongoDB\BSON\Decimal128(NAN));
var_dump((string) new MongoDB\BSON\Decimal128(INF));

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(9) "1234.5678"
string(3) "NaN"
string(8) "Infinity"
```

### Дивіться також

-   [» Формат з плаваючою точкою Decimal128](https://en.wikipedia.org/wiki/Decimal128_floating-point_format)
-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)