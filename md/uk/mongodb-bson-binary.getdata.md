---
navigation:
  - mongodb-bson-binary.construct.md: '« MongoDB\\BSON\\Binary::\_\_construct'
  - mongodb-bson-binary.gettype.md: 'MongoDB\\BSON\\Binary::getType »'
  - index.md: PHP Manual
  - class.mongodb-bson-binary.md: MongoDB\\BSON\\Binary
title: 'MongoDB\\BSON\\Binary::getData'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Binary::getData

(mongodb >=1.0.0)

MongoDB\\BSON\\Binary::getData — Повертає дані Binary

### Опис

```methodsynopsis
final public MongoDB\BSON\Binary::getData(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає дані Binary.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання** MongoDB\\BSON\\Binary::getData()\*\*\*\*

```php
<?php

$binary = new MongoDB\BSON\Binary('foo', MongoDB\BSON\Binary::TYPE_GENERIC);
var_dump($binary->getData());

?>
```

Результат виконання наведеного прикладу:

```
string(3) "foo"
```

### Дивіться також

-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
