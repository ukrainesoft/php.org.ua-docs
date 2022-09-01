---
navigation:
  - mongodb-bson-javascript.serialize.html: '« MongoDBBSONJavascript::serialize'
  - mongodb-bson-javascript.unserialize.html: 'MongoDBBSONJavascript::unserialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-javascript.html: MongoDBBSONJavascript
title: 'MongoDBBSONJavascript::toString'
---
# MongoDBBSONJavascript::toString

(mongodb >=1.2.0)

MongoDBBSONJavascript::toString — Повертає код JavaScript

### Опис

```methodsynopsis
final public MongoDB\BSON\Javascript::__toString(): string
```

Цей метод є псевдонімом: [MongoDBBSONJavascript::getCode()](mongodb-bson-javascript.getcode.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає JavaScript.

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONJavascript::toString()****

```php
<?php

var_dump((string) new MongoDB\BSON\Javascript('function foo(bar) { return bar; }'));

?>
```

Результат виконання цього прикладу:

```
string(33) "function foo(bar) { return bar; }"
```

### Дивіться також

-   [MongoDBBSONJavascript::getCode()](mongodb-bson-javascript.getcode.html) - Повертає код JavaScript
-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
