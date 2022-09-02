---
navigation:
  - mongodb-bson-utcdatetime.todatetime.md: '« MongoDBBSONUTCDateTime::toDateTime'
  - mongodb-bson-utcdatetime.unserialize.md: 'MongoDBBSONUTCDateTime::unserialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-utcdatetime.md: MongoDBBSONUTCDateTime
title: 'MongoDBBSONUTCDateTime::function toString() { \[native code\] }'
---
# MongoDBBSONUTCDateTime::function toString() { \[native code\] }

(mongodb >=1.0.0)

MongoDBBSONUTCDateTime::toString — Повертає рядкову виставу UTCDateTime

### Опис

```methodsynopsis
final public MongoDB\BSON\UTCDateTime::__toString(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядкову виставу UTCDateTime.

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONUTCDateTime::toString()****

```php
<?php

$utcdatetime = new MongoDB\BSON\UTCDateTime(1416445411987);
var_dump((string) $utcdatetime);

?>
```

Результат виконання цього прикладу:

```
string(13) "1416445411987"
```

### Дивіться також

-   [» Типи BSON: Date](https://www.mongodb.com/docs/manual/reference/bson-types/#date)
