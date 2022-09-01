---
navigation:
  - mongodb-bson-binary.serialize.html: '« MongoDBBSONBinary::serialize'
  - mongodb-bson-binary.unserialize.html: 'MongoDBBSONBinary::unserialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-binary.html: MongoDBBSONBinary
title: 'MongoDBBSONBinary::toString'
---
# MongoDBBSONBinary::toString

(mongodb >=1.2.0)

MongoDBBSONBinary::toString — Повертає дані Binary

### Опис

```methodsynopsis
final public MongoDB\BSON\Binary::__toString(): string
```

Цей метод є псевдонімом: [MongoDBBSONBinary::getData()](mongodb-bson-binary.getdata.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає дані Binary.

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONBinary::toString()****

```php
<?php

var_dump((string) new MongoDB\BSON\Binary('foo', MongoDB\BSON\Binary::TYPE_GENERIC));

?>
```

Результат виконання цього прикладу:

```
string(3) "foo"
```

### Дивіться також

-   [MongoDBBSONBinary::getData()](mongodb-bson-binary.getdata.md) - Повертає дані Binary
-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
