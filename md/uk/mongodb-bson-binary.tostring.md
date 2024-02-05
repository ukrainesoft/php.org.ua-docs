---
navigation:
  - mongodb-bson-binary.serialize.md: '« MongoDB\\BSON\\Binary::serialize'
  - mongodb-bson-binary.unserialize.md: 'MongoDB\\BSON\\Binary::unserialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-binary.md: MongoDB\\BSON\\Binary
title: 'MongoDB\\BSON\\Binary::\_\_function toString() { \[native code\] }'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Binary::\_\_function toString() { \[native code\] }

(mongodb >=1.2.0)

MongoDB\\BSON\\Binary::\_\_toString — Повертає дані Binary

### Опис

```methodsynopsis
final public MongoDB\BSON\Binary::__toString(): string
```

Метод — псевдоним метода:[MongoDB\\BSON\\Binary::getData()](mongodb-bson-binary.getdata.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає дані Binary.

### Приклади

**Пример #1 Пример использования**MongoDB\\BSON\\Binary::\_\_toString()\*\*\*\*

```php
<?php

var_dump((string) new MongoDB\BSON\Binary('foo', MongoDB\BSON\Binary::TYPE_GENERIC));

?>
```

Результат виконання наведеного прикладу:

```
string(3) "foo"
```

### Дивіться також

-   [MongoDB\\BSON\\Binary::getData()](mongodb-bson-binary.getdata.md) \- Повертає дані Binary
-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
