---
navigation:
  - mongodb-bson-objectid.serialize.md: '« MongoDBBSONObjectId::serialize'
  - mongodb-bson-objectid.unserialize.md: 'MongoDBBSONObjectId::unserialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-objectid.md: MongoDBBSONObjectId
title: 'MongoDBBSONObjectId::function toString() { \[native code\] }'
---
# MongoDBBSONObjectId::function toString() { \[native code\] }

(mongodb >=1.0.0)

MongoDBBSONObjectId::toString — Повертає шістнадцяткову виставу ObjectId

### Опис

```methodsynopsis
final public MongoDB\BSON\ObjectId::__toString(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає шістнадцяткову виставу ObjectId.

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONObjectId::toString()****

```php
<?php

var_dump((string) new MongoDB\BSON\ObjectId());
var_dump((string) new MongoDB\BSON\ObjectId('000000000000000000000001'));

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(24) "56731b49da14d8747d701211"
string(24) "000000000000000000000001"
```

### Дивіться також

-   [» Справка по ObjectId](https://www.mongodb.com/docs/manual/reference/bson-types/#objectid)
-   [» Типи BSON: ObjectId](https://www.mongodb.com/docs/manual/reference/bson-types/#objectid)
