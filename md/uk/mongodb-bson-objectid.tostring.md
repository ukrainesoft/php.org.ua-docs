---
navigation:
  - mongodb-bson-objectid.serialize.md: '« MongoDB\\BSON\\ObjectId::serialize'
  - mongodb-bson-objectid.unserialize.md: 'MongoDB\\BSON\\ObjectId::unserialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-objectid.md: MongoDB\\BSON\\ObjectId
title: 'MongoDB\\BSON\\ObjectId::\_\_function toString() { \[native code\] }'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\ObjectId::\_\_function toString() { \[native code\] }

(mongodb >=1.0.0)

MongoDB\\BSON\\ObjectId::\_\_toString — Повертає шістнадцяткову виставу ObjectId

### Опис

```methodsynopsis
final public MongoDB\BSON\ObjectId::__toString(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає шістнадцяткову виставу ObjectId.

### Приклади

**Пример #1 Пример использования**MongoDB\\BSON\\ObjectId::\_\_toString()\*\*\*\*

```php
<?php

var_dump((string) new MongoDB\BSON\ObjectId());
var_dump((string) new MongoDB\BSON\ObjectId('000000000000000000000001'));

?>
```

Висновок наведеного прикладу буде схожим на:

```
string(24) "56731b49da14d8747d701211"
string(24) "000000000000000000000001"
```

### Дивіться також

-   [» Довідка по ObjectId](https://www.mongodb.com/docs/manual/reference/bson-types/#objectid)
-   [» Типи BSON: ObjectId](https://www.mongodb.com/docs/manual/reference/bson-types/#objectid)
