---
navigation:
  - class.mongodb-bson-objectid.md: « MongoDB\\BSON\\ObjectId
  - mongodb-bson-objectid.gettimestamp.md: 'MongoDB\\BSON\\ObjectId::getTimestamp »'
  - index.md: PHP Manual
  - class.mongodb-bson-objectid.md: MongoDB\\BSON\\ObjectId
title: 'MongoDB\\BSON\\ObjectId::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\ObjectId::\_\_construct

(mongodb >=1.0.0)

MongoDB\\BSON\\ObjectId::\_\_construct — Створює новий ObjectId

### Опис

```methodsynopsis
final public MongoDB\BSON\ObjectId::__construct(?string $id = null)
```

### Список параметрів

`id`(string)

24-символьний шістнадцятковий рядок. Якщо зазначено, драйвер згенерує ObjectId.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Видає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md) якщо `id`не є 24-символьним шістнадцятковим рядком.

### Приклади

**Пример #1 Пример использования**MongoDB\\BSON\\ObjectId::\_\_construct()\*\*\*\*

```php
<?php

var_dump(new MongoDB\BSON\ObjectId());

var_dump(new MongoDB\BSON\ObjectId('000000000000000000000001'));

?>
```

Висновок наведеного прикладу буде схожим на:

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

-   [» Довідка по ObjectId](https://www.mongodb.com/docs/manual/reference/bson-types/#objectid)
-   [» Типи BSON: ObjectId](https://www.mongodb.com/docs/manual/reference/bson-types/#objectid)
