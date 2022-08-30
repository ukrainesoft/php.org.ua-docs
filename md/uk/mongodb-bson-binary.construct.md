Створює новий Binary

-   [« MongoDBBSONBinary](class.mongodb-bson-binary.html)
    
-   [MongoDBBSONBinary::getData »](mongodb-bson-binary.getdata.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBBSONBinary](class.mongodb-bson-binary.html)
    
-   Створює новий Binary
    

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

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Видає [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html), якщо `type` не є 8-розрядним цілим числом.
-   Видає [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html), якщо `type` є **`MongoDB\BSON\Binary::TYPE_UUID`** або **`MongoDB\BSON\Binary::TYPE_OLD_UUID`**, а довжина `data` не дорівнює 16 байтам.

### список змін

| Версия                                                                                                                                                                                                                                                             | Описание |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|
| PECL mongodb 1.3.0                                                                                                                                                                                                                                                 |          |
| [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html) видається, якщо `type` є **`MongoDB\BSON\Binary::TYPE_UUID`** або **`MongoDB\BSON\Binary::TYPE_OLD_UUID`**, а довжина `data` не дорівнює 16 байтам. |          |

| | PECL mongodb 1.1.3 |

[MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html) видається, якщо `type` не є 8-розрядним цілим числом.

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

-   [» Типы BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)