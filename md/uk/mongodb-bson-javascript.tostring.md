---
navigation:
  - mongodb-bson-javascript.serialize.md: '« MongoDB\\BSON\\Javascript::serialize'
  - mongodb-bson-javascript.unserialize.md: 'MongoDB\\BSON\\Javascript::unserialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-javascript.md: MongoDB\\BSON\\Javascript
title: 'MongoDB\\BSON\\Javascript::\_\_function toString() { \[native code\] }'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Javascript::\_\_function toString() { \[native code\] }

(mongodb >=1.2.0)

MongoDB\\BSON\\Javascript::\_\_toString — Повертає код JavaScript

### Опис

```methodsynopsis
final public MongoDB\BSON\Javascript::__toString(): string
```

Метод — псевдоним метода:[MongoDB\\BSON\\Javascript::getCode()](mongodb-bson-javascript.getcode.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає JavaScript.

### Приклади

**Пример #1 Пример использования**MongoDB\\BSON\\Javascript::\_\_toString()\*\*\*\*

```php
<?php

var_dump((string) new MongoDB\BSON\Javascript('function foo(bar) { return bar; }'));

?>
```

Результат виконання наведеного прикладу:

```
string(33) "function foo(bar) { return bar; }"
```

### Дивіться також

-   [MongoDB\\BSON\\Javascript::getCode()](mongodb-bson-javascript.getcode.md) \- Повертає код JavaScript
-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
