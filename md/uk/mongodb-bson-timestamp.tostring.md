---
navigation:
  - mongodb-bson-timestamp.serialize.html: '« MongoDBBSONTimestamp::serialize'
  - mongodb-bson-timestamp.unserialize.html: 'MongoDBBSONTimestamp::unserialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-timestamp.html: MongoDBBSONTimestamp
title: 'MongoDBBSONTimestamp::function toString() { \[native code\] }'
---
# MongoDBBSONTimestamp::function toString() { \[native code\] }

(mongodb >=1.0.0)

MongoDBBSONTimestamp::toString — Повертає строкову виставу Timestamp

### Опис

```methodsynopsis
final public MongoDB\BSON\Timestamp::__toString(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядкову виставу Timestamp.

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONTimestamp::toString()****

```php
<?php

$timestamp = new MongoDB\BSON\Timestamp(1234, 5678);
var_dump((string) $timestamp);

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(11) "[1234:5678]"
```

### Дивіться також

-   [» Типи BSON: Timestamps](https://www.mongodb.com/docs/manual/reference/bson-types/#timestamps)
