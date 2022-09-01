---
navigation:
  - mongodb-bson-int64.serialize.html: '« MongoDBBSONInt64::serialize'
  - mongodb-bson-int64.unserialize.html: 'MongoDBBSONInt64::unserialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-int64.html: MongoDBBSONInt64
title: 'MongoDBBSONInt64::toString'
---
# MongoDBBSONInt64::toString

(mongodb >=1.5.0)

MongoDBBSONInt64::toString — Повертає рядкову виставу Int64

### Опис

```methodsynopsis
final public MongoDB\BSON\Int64::__toString(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядкову виставу Int64.

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONInt64::toString()****

```php
<?php

$int64 = unserialize('C:18:"MongoDB\BSON\Int64":47:{a:1:{s:7:"integer";s:19:"9223372036854775807";}}');

var_dump((string) $int64);

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(19) "9223372036854775807"
```

### Дивіться також

-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
