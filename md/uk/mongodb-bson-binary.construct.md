---
navigation:
  - class.mongodb-bson-binary.md: « MongoDB\\BSON\\Binary
  - mongodb-bson-binary.getdata.md: 'MongoDB\\BSON\\Binary::getData »'
  - index.md: PHP Manual
  - class.mongodb-bson-binary.md: MongoDB\\BSON\\Binary
title: 'MongoDB\\BSON\\Binary::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Binary::\_\_construct

(mongodb >=1.0.0)

MongoDB\\BSON\\Binary::\_\_construct — Створює новий Binary

### Опис

```methodsynopsis
final public MongoDB\BSON\Binary::__construct(string $data, int $type = MongoDB\BSON\Binary::TYPE_GENERIC)
```

### Список параметрів

`data`(string)

Двійкові дані.

`type`(int)

8-розрядне ціле число, що означає тип даних. За замовчуванням набуває значення \*\*`MongoDB\BSON\Binary::TYPE_GENERIC`\*\*якщо не вказано.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Видає[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md), якщо `type` не є 8-розрядним цілим числом.
-   Видає[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md), якщо `type`является\*\*`MongoDB\BSON\Binary::TYPE_UUID`** або **`MongoDB\BSON\Binary::TYPE_OLD_UUID`\*\*, а длина`data`не равна 16 байтам.

### список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.15.0 |  |
| Параметр`type` за замовчуванням набуває значення **`MongoDB\BSON\Binary::TYPE_GENERIC`**, якщо не вказано. |  |

| | PECL mongodb 1.3.0 |

[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md) видається, якщо `type`является\*\*`MongoDB\BSON\Binary::TYPE_UUID`** або **`MongoDB\BSON\Binary::TYPE_OLD_UUID`\*\*, а длина`data`не равна 16 байтам.

| | PECL mongodb 1.1.3 |

[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md) видається, якщо `type` не є 8-розрядним цілим числом.

### Приклади

**Приклад #1 Приклад використання** MongoDB\\BSON\\Binary::\_\_construct()\*\*\*\*

```php
<?php

$binary = new MongoDB\BSON\Binary('foo', MongoDB\BSON\Binary::TYPE_GENERIC);
var_dump($binary);

?>
```

Результат виконання наведеного прикладу:

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
