---
navigation:
  - mongodb-bson-binary.construct.md: '« MongoDBBSONBinary::construct'
  - mongodb-bson-binary.gettype.md: 'MongoDBBSONBinary::getType »'
  - index.md: PHP Manual
  - class.mongodb-bson-binary.md: MongoDBBSONBinary
title: 'MongoDBBSONBinary::getData'
---
# MongoDBBSONBinary::getData

(mongodb >=1.0.0)

MongoDBBSONBinary::getData — Повертає дані Binary

### Опис

```methodsynopsis
final public MongoDB\BSON\Binary::getData(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає дані Binary.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONBinary::getData()****

```php
<?php

$binary = new MongoDB\BSON\Binary('foo', MongoDB\BSON\Binary::TYPE_GENERIC);
var_dump($binary->getData());

?>
```

Результат виконання цього прикладу:

```
string(3) "foo"
```

### Дивіться також

-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
