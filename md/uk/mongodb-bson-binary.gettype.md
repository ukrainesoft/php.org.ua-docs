---
navigation:
  - mongodb-bson-binary.getdata.md: '« MongoDB\\BSON\\Binary::getData'
  - mongodb-bson-binary.jsonserialize.md: 'MongoDB\\BSON\\Binary::jsonSerialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-binary.md: MongoDB\\BSON\\Binary
title: 'MongoDB\\BSON\\Binary::getType'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Binary::getType

(mongodb >=1.0.0)

MongoDB\\BSON\\Binary::getType — Повертає тип Binary

### Опис

```methodsynopsis
final public MongoDB\BSON\Binary::getType(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає тип Binary.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Пример #1 Пример использования**MongoDB\\BSON\\Binary::getType()\*\*\*\*

```php
<?php

$binary = new MongoDB\BSON\Binary('foo', MongoDB\BSON\Binary::TYPE_GENERIC);
var_dump($binary->getType());

?>
```

Результат виконання наведеного прикладу:

```
int(0)
```

### Дивіться також

-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
