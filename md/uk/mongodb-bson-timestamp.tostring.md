---
navigation:
  - mongodb-bson-timestamp.serialize.md: '« MongoDB\\BSON\\Timestamp::serialize'
  - mongodb-bson-timestamp.unserialize.md: 'MongoDB\\BSON\\Timestamp::unserialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-timestamp.md: MongoDB\\BSON\\Timestamp
title: 'MongoDB\\BSON\\Timestamp::\_\_function toString() { \[native code\] }'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Timestamp::\_\_function toString() { \[native code\] }

(mongodb >=1.0.0)

MongoDB\\BSON\\Timestamp::\_\_toString — Повертає строкову виставу Timestamp

### Опис

```methodsynopsis
final public MongoDB\BSON\Timestamp::__toString(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядкову виставу Timestamp.

### Приклади

**Пример #1 Пример использования**MongoDB\\BSON\\Timestamp::\_\_toString()\*\*\*\*

```php
<?php

$timestamp = new MongoDB\BSON\Timestamp(1234, 5678);
var_dump((string) $timestamp);

?>
```

Висновок наведеного прикладу буде схожим на:

```
string(11) "[1234:5678]"
```

### Дивіться також

-   [» Типи BSON: Timestamps](https://www.mongodb.com/docs/manual/reference/bson-types/#timestamps)
