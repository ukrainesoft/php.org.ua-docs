---
navigation:
  - mongodb-bson-int64.serialize.md: '« MongoDB\\BSON\\Int64::serialize'
  - mongodb-bson-int64.unserialize.md: 'MongoDB\\BSON\\Int64::unserialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-int64.md: MongoDB\\BSON\\Int64
title: 'MongoDB\\BSON\\Int64::\_\_function toString() { \[native code\] }'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Int64::\_\_function toString() { \[native code\] }

(mongodb >=1.5.0)

MongoDB\\BSON\\Int64::\_\_toString — Повертає рядкову виставу Int64

### Опис

```methodsynopsis
final public MongoDB\BSON\Int64::__toString(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядкову виставу Int64.

### Приклади

**Пример #1 Пример использования**MongoDB\\BSON\\Int64::\_\_toString()\*\*\*\*

```php
<?php

$int64 = new MongoDB\BSON\Int64('9223372036854775807');

var_dump((string) $int64);

?>
```

Висновок наведеного прикладу буде схожим на:

```
string(19) "9223372036854775807"
```

### Дивіться також

-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
