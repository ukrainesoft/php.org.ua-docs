---
navigation:
  - class.mongodb-bson-binary.html: « MongoDBBSONBinary
  - mongodb-bson-binary.getdata.html: 'MongoDBBSONBinary::getData »'
  - index.md: PHP Manual
  - class.mongodb-bson-binary.html: MongoDBBSONBinary
title: 'MongoDBBSONBinary::construct'
---
# MongoDBBSONBinary::construct

(mongodb >=1.0.0)

MongoDBBSONBinary::construct — Створює новий Binary

### Опис

```methodsynopsis
final public MongoDB\BSON\Binary::__construct(string $data, int $type)
```

### Список параметрів

`data` (string)

Двійкові дані.

`type` (int)

8-розрядне ціле число, що означає тип даних.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Видає [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md), якщо `type` не є 8-розрядним цілим числом.
-   Видає [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md), якщо `type` є **`MongoDB\BSON\Binary::TYPE_UUID`** або **`MongoDB\BSON\Binary::TYPE_OLD_UUID`**, а довжина `data` не дорівнює 16 байтам.

### список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.3.0 |  |
| [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md) видається, якщо `type` є **`MongoDB\BSON\Binary::TYPE_UUID`** або **`MongoDB\BSON\Binary::TYPE_OLD_UUID`**, а довжина `data` не дорівнює 16 байтам. |  |

| | PECL mongodb 1.1.3 |

[MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md) видається, якщо `type` не є 8-розрядним цілим числом.

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONBinary::construct()****

```php
<?php

$binary = new MongoDB\BSON\Binary('foo', MongoDB\BSON\Binary::TYPE_GENERIC);
var_dump($binary);

?>
```

Результат виконання цього прикладу:

```
object(MongoDB\BSON\Binary)#1 (2) {
  ["data"]=>
  string(3) "foo"
  ["type"]=>
  int(0)
}
```

### Дивіться також

-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
