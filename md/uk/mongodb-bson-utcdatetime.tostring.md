---
navigation:
  - mongodb-bson-utcdatetime.todatetime.md: '« MongoDB\\BSON\\UTCDateTime::toDateTime'
  - mongodb-bson-utcdatetime.unserialize.md: 'MongoDB\\BSON\\UTCDateTime::unserialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-utcdatetime.md: MongoDB\\BSON\\UTCDateTime
title: 'MongoDB\\BSON\\UTCDateTime::\_\_function toString() { \[native code\] }'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\UTCDateTime::\_\_function toString() { \[native code\] }

(mongodb >=1.0.0)

MongoDB\\BSON\\UTCDateTime::\_\_toString — Повертає рядкову виставу UTCDateTime

### Опис

```methodsynopsis
final public MongoDB\BSON\UTCDateTime::__toString(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядкову виставу UTCDateTime.

### Приклади

**Приклад #1 Приклад використання** MongoDB\\BSON\\UTCDateTime::\_\_toString()\*\*\*\*

```php
<?php

$utcdatetime = new MongoDB\BSON\UTCDateTime(1416445411987);
var_dump((string) $utcdatetime);

?>
```

Результат виконання наведеного прикладу:

```
string(13) "1416445411987"
```

### Дивіться також

-   [» Типи BSON: Date](https://www.mongodb.com/docs/manual/reference/bson-types/#date)
