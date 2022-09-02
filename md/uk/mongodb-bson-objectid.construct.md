---
navigation:
  - class.mongodb-bson-objectid.md: « MongoDBBSONObjectId
  - mongodb-bson-objectid.gettimestamp.md: 'MongoDBBSONObjectId::getTimestamp »'
  - index.md: PHP Manual
  - class.mongodb-bson-objectid.md: MongoDBBSONObjectId
title: 'MongoDBBSONObjectId::construct'
---
# MongoDBBSONObjectId::construct

(mongodb >=1.0.0)

MongoDBBSONObjectId::construct — Створює новий ObjectId

### Опис

```methodsynopsis
final public MongoDB\BSON\ObjectId::__construct(?string $id = null)
```

### Список параметрів

`id` (string)

24-символьний шістнадцятковий рядок. Якщо зазначено, драйвер згенерує ObjectId.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Видає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md) якщо `id` не є 24-символьним шістнадцятковим рядком.

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONObjectId::construct()****

```php
<?php

var_dump(new MongoDB\BSON\ObjectId());

var_dump(new MongoDB\BSON\ObjectId('000000000000000000000001'));

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(MongoDB\BSON\ObjectId)#1 (1) {
  ["oid"]=>
  string(24) "56732d3dda14d81214634921"
}
object(MongoDB\BSON\ObjectId)#1 (1) {
  ["oid"]=>
  string(24) "000000000000000000000001"
}
```

### Дивіться також

-   [» Справка по ObjectId](https://www.mongodb.com/docs/manual/reference/bson-types/#objectid)
-   [» Типи BSON: ObjectId](https://www.mongodb.com/docs/manual/reference/bson-types/#objectid)
