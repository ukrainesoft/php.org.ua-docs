---
navigation:
  - mongodb-bson-regex.serialize.md: '« MongoDB\\BSON\\Regex::serialize'
  - mongodb-bson-regex.unserialize.md: 'MongoDB\\BSON\\Regex::unserialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-regex.md: MongoDB\\BSON\\Regex
title: 'MongoDB\\BSON\\Regex::\_\_function toString() { \[native code\] }'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Regex::\_\_function toString() { \[native code\] }

(mongodb >=1.0.0)

MongoDB\\BSON\\Regex::\_\_toString — Повертає рядкову виставу Regex

### Опис

```methodsynopsis
final public MongoDB\BSON\Regex::__toString(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядкову виставу Regex.

### Приклади

**Приклад #1 Приклад використання** MongoDB\\BSON\\Regex::\_\_toString()\*\*\*\*

```php
<?php

$regex = new MongoDB\BSON\Regex('regex', 'i');
var_dump((string) $regex);

?>
```

Результат виконання наведеного прикладу:

```
string(8) "/regex/i"
```

### Дивіться також

-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
